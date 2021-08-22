---
description: Das Microsoft Windows Software Development Kit (SDK) enthält lokalisierte Ressourcenzeichenfolgen, lokalisierte Fehlertabellen und lokalisierte ActionText-Tabellen für die in der folgenden Tabelle aufgeführten Sprachen.
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: Lokalisieren der Tabellen "Error" und "ActionText"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1839141b80afd1d28aa9e9317da10d79aea41232f9e7ebde0db7971d22f5141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629465"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>Lokalisieren der Tabellen "Error" und "ActionText"

Das Microsoft Windows Software Development Kit (SDK) enthält lokalisierte [](error-table.md)Ressourcenzeichenfolgen, lokalisierte Fehlertabellen und lokalisierte [ActionText-Tabellen](actiontext-table.md) für die in der folgenden Tabelle aufgeführten Sprachen. Die mit Sternchen markierten LANGIDs geben an, dass die Ressourcenzeichenfolgen als Basissprache gespeichert werden und daher mit allen Dialekten dieser Sprache verwendet werden können.

Sie können die lokalisierten Tabellen Error und ActionText in Ihre Datenbank importieren, indem Sie Msidb.exe [**oder MsiDatabaseImport verwenden.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)



| LANGID (dezimal) | LANGID (hexadezimal) | ASCII-Codepage | Abkürzung | Sprache                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | Ara          | Arabisch - Saudi-Arabien         | ar-SA            |
| 1027             | 0x403                | 1252            | Katze          | Katalanisch                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | Chinesisch (Taiwan)              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | Chinesisch (China)               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | Tschechisch – PragerIsche Republik        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | Norwegen – Spanien               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | Deutsch - Deutschland              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | Griechisch – Griechisch                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | German - Germany       | en-US            |
| 3082\*           | 0xC0A                | 1252            | ESN          | Spanisch – Moderne Sortierung – Spanien | es-ES            |
| 1061             | 0x425                | 1257            | CIM          | Estnisch                      | et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | Finnisch – Norwegen             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | Französisch - Frankreich               | fr-FR            |
| 1037             | 0x40D                | 1255            | Heb          | Hebräisch – Hebräisch               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | Italienisch – Spanien           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | Italienisch – Italien               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | Japanisch - Japan              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | Koreanisch - Korea                | ko-KO            |
| 1063             | 0x427                | 1257            | Lth          | Litauisch                    | lt-LT            |
| 1062             | 0x426                | 1257            | Lvi          | Lettisch                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | Niederländisch – Niederlande           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | Norwegisch (Bokm): Norwegen    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | Polnisch – Polnisch               | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | Portugiesisch (Brasilien)           | pt-BR            |
| 2070             | 0x816                | 1252            | PTG          | Portugiesisch (Portugal)         | pt-PT            |
| 1048             | 0x418                | 1250            | ROM          | 2017 – 2017            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | Russisch - Russische Föderation              | ru-RU            |
| 1050             | 0x41A                | 1250            | Hrv          | Kroatisch – Serbisch            | hr-HR            |
| 1051             | 0x41B                | 1250            | Himmel          | Slowakisch – Slowakisch             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | Schwedisch – Spanien              | sv-SE            |
| 1054             | 0x41E                | 874             | Tha          | Thailändisch – Thailändisch               | th-TH            |
| 1.055             | 0x41F                | 1254            | TRK          | Türkisch – Türkisch              | tr-TR            |
| 1060             | 0x424                | 1250            | Slv          | Slowenisch – Slowenisch          | sl-SI            |
| 1066             | 0x42A                | 1258            | Vit          | Gossisch –Gossisch Nam         | vi-VN            |
| 1069             | 0x42D                | 1252            | EUQ          | Baskisch (Baskenland)               | eu-ES            |



 

**Windows Vista:** Zusätzlich zu den in der vorherigen Tabelle aufgeführten Sprachen sind die Sprachen in der folgenden Tabelle ab Windows Vista verfügbar.



| LANGID (dezimal) | LANGID (hexadezimal) | ASCII-Codepage | Abkürzung | Sprache        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BGR          | Bulgarisch       | bg-BG            |
| 1058             | 0x422                | 1251            | Ukr          | Ukrainisch       | uk-UA            |
| 2074             | 0x81A                | 1250            | Srl          | Serbisch (Lateinisch) | sr-Latn-CS       |



 

 

 



