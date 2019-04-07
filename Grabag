const MailListener = require("mail-listener2
const cheerio = require("cheerio");
const fs = require("async-file");
const moment = require("moment");
const readline = require("readline-sync");

console.log("$$$$$$$$$$$$$$$$$$");
console.log("You Sell I am Buy");
console.log("$$$$$$$$$$$$$$$$$$");

console.log("");
console.log("");

const emel = readline.question("Masukan user
const password = readline.question("Masukan

const mailListener = new MailListener({
username: emel,
password: password,
host: "imap.gmail.com",
port: 993, // imap port
tls: true,
connTimeout: 10000, // Default by node-ima
authTimeout: 5000, // Default by node-imap
debug: console.log, // Or your custom func
tlsOptions: { rejectUnauthorized: false },
mailbox: "INBOX", // mailbox to monitor
searchFilter: ["ALL", ["SUBJECT", "BIGtoke
markSeen: true, // all fetched email willb
fetchUnreadOnStart: true, // use it only i
mailParserOptions: { streamAttachments: tr
attachments: true, // download attachments
attachmentOptions: { directory: "attachmen
});
mailListener.start(); // start listening

// stop listening
//mailListener.stop();

mailListener.on("server:connected", function
console.log("imapConnected");
});

mailListener.on("server:disconnected", funct
console.log("imapDisconnected");
});

mailListener.on("mail", function(mail, seqno
// do something with mail object including

const $ = cheerio.load(mail.html);
const src = $(".button").attr("href");
fs.appendFile("result_gmail.txt", `${src}\
console.log(
"[" +
" " +
moment().format("HH:mm:ss") +
" " +
"]" +
" " +
"Lokasi Link :" +
" " +
`grabag.txt`
);
// mail processing code goes here
});
