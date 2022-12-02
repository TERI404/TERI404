const Discord = require("discord.js");

// Discord botを作成する
const bot = new Discord.Client();

// botが起動したときの処理
bot.on("ready", () => {
  console.log("Bot is ready!");
});

// メッセージが送信されたときの処理
bot.on("message", (message) => {
  // メッセージが「かお、」を含む場合
  if (message.content.includes("かお、")) {
    // 絵文字を付ける
    message.react("");
  }
});

// botを起動する
bot.login("[BOT_TOKEN]");
