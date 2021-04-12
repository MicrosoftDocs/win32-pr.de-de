---
description: Das Microsoft Windows Software Development Kit (SDK) umfasst lokalisierte Ressourcen Zeichenfolgen, lokalisierte Fehler Tabellen und lokalisierte Aktions Text Tabellen für die Sprachen, die in der folgenden Tabelle aufgeführt sind.
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: Lokalisieren von Fehler-und Aktions Text Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c45428d9f0d3c4b8dcafbf489f7316225a83f032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346318"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>Lokalisieren von Fehler-und Aktions Text Tabellen

Das Microsoft Windows Software Development Kit (SDK) umfasst lokalisierte Ressourcen Zeichenfolgen, lokalisierte [Fehler Tabellen](error-table.md)und lokalisierte [Aktions Text Tabellen](actiontext-table.md) für die Sprachen, die in der folgenden Tabelle aufgeführt sind. Die mit Sternchen markierten langids zeigen an, dass die Ressourcen Zeichenfolgen als Basis Sprache gespeichert werden und mit allen Dialekten dieser Sprache verwendet werden können.

Sie können die lokalisierten Fehler-und Aktions Text Tabellen mithilfe von Msidb.exe oder [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)in die-Datenbank importieren.



| Langid (Decimal) | Langid (hexadezimal) | ASCII-Codepage | Abkürzung | Sprache                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | Genannt          | Arabisch - Saudi-Arabien         | ar-SA            |
| 1027             | 0x403                | 1252            | Cat          | Katalanisch                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | Chinesisch (Taiwan)              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | Chinesisch (China)               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | Tschechische Republik        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | Dänisch-Dänemark               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | Deutsch - Deutschland              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | Griechisch (Griechenland)                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | German - Germany       | de-DE            |
| 3082\*           | 0xC0A                | 1252            | ESN          | Spanisch-modern Sort-Spanien | es-ES            |
| 1061             | 0x425                | 1257            | ETI          | Estnisch                      | et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | Finnisch (Finnland)             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | Französisch - Frankreich               | fr-FR            |
| 1037             | 0x40d                | 1255            | Heb          | Hebräisch (Israel)               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | Ungarisch-Ungarn           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | Italienisch – Italien               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | Japanisch - Japan              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | Koreanisch - Korea                | Ko-Ko            |
| 1063             | 0x427                | 1257            | LTH          | Litauisch                    | lt-LT            |
| 1062             | Thomas.Axen@Domäne.com                | 1257            | LVI          | Lettisch                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | Niederländisch – Niederlande           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | Norwegisch (Bokmål)-Norwegen    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | Polnisch-Polen               | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | Portugiesisch (Brasilien)           | pt-BR            |
| 2070             | 0x816                | 1252            | PTG          | Portugiesisch (Portugal)         | pt-PT            |
| 1048             | 0x418                | 1250            | Strom          | Rumänisch (Rumänien)            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | Russisch - Russische Föderation              | ru-RU            |
| 1050             | 0x41A                | 1250            | HRV          | Kroatisch (Kroatien)            | hr-HR            |
| 1051             | 0x41b                | 1250            | Ski          | Slowakisch (Slowakei)             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | Schwedisch-Schweden              | sv-SE            |
| 1054             | 0x41e                | 874             | Gesteckt          | Thailändisch (Thailand)               | th-TH            |
| 1.055             | 0x41F                | 1254            | TRK          | Türkisch-Türkei              | tr-TR            |
| 1060             | 0x424                | 1250            | SLV          | Slowenisch (Slowenien)          | sl-SI            |
| 1066             | 0x42a                | 1258            | Umgewandelt          | Vietnamesisch-Vietnam         | vi-VN            |
| 1069             | 0x42d                | 1252            | Euq          | Baskisch (Baskenland)               | eu-ES            |



 

**Windows Vista:** Zusätzlich zu den in der vorherigen Tabelle aufgeführten Sprachen sind die Sprachen in der folgenden Tabelle ab Windows Vista verfügbar.



| Langid (Decimal) | Langid (hexadezimal) | ASCII-Codepage | Abkürzung | Sprache        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BGR          | Bulgarisch       | bg-BG            |
| 1058             | 0x422                | 1251            | UKR          | Ukrainisch       | uk-UA            |
| 2074             | 0x81a                | 1250            | SRL          | Serbisch (Lateinisch) | sr-Latn-CS       |



 

 

 



