---
description: In diesem Thema werden Bezeichner für die Sortierreihenfolge beschrieben, die bei der Vorbereitung von Gebiets Schema Bezeichners verwendet werden können.
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: Sortierreihenfolge-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349788"
---
# <a name="sort-order-identifiers"></a>Sortierreihenfolge-IDs

In diesem Thema werden Bezeichner für die Sortierreihenfolge beschrieben, die bei [der Vorbereitung von Gebiets](locale-identifiers.md)Schema Bezeichners verwendet werden können. Eine Sortierreihenfolge-ID wird in der Form " \_ sortor" am Ende des Gebiets Schema namens definiert, der im Bezeichner verwendet wird, z. b. "de-de \_ phoneb", wobei "phoneb" die Sortierreihenfolge ist. Der entsprechende Gebiets Schema Bezeichner wird wie folgt erstellt: `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` .



| Konstante                      | Gebiets Schema Name                                                                                         | Bedeutung                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| \_Chinesisch ( \_ Big5) Sortieren           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Chinesisch (Big5)                                                |
| \_Chinesisch ( \_ Bopomofo) Sortieren       | zh-tw \_ pronun                                                                                       | Chinesisch (traditionell) Bopomofo-Bestellung                                |
| \_chinesisches \_ Telefon \_ Buch sortieren    | zh-CN \_ phoneb<br/>                                                                            | Chinesische Telefonbuch Bestellung (Nachname)                                |
| \_chinesische \_ Volksrepublik China sortieren            | zh-CN- \_ Strich<br/> ZH-HK- \_ Strich<br/> ZH-Mo- \_ Strich<br/> ZH-SG- \_ Strich<br/> | Volksrepublik China (chinesische Strich Anzahl)                                    |
| \_Chinesisch- \_ PRCP sortieren           | zh-CN<br/> zh-SG<br/>                                                                   | Volksrepublik China, phonetische Reihenfolge                                        |
| \_chinesischen \_ radicalstroke sortieren  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Chinesisch (radikal/Strich)                                      |
| \_Chinesisch ( \_ Unicode) Sortieren        | —                                                                                                   | Chinesische Unicode-Bestellung **Windows 2000:** nicht unterstützt.<br/>  |
| \_Standard sortieren                 | Der Name des Gebiets Schemas, das mit dem entsprechenden Sprachnamen identisch ist.                                     | Standardsortierspalte                                                |
| \_GEORGIAN \_ modern sortieren        | ka-ge \_ modern                                                                                       | Georgische moderne Reihenfolge                                             |
| \_georgisches \_ traditionelles sortieren   | ka-GE                                                                                               | Georgische herkömmliche Reihenfolge                                        |
| \_Deutsches \_ Telefon \_ Buch sortieren     | de-de \_ phoneb                                                                                       | Deutsche Telefonbuch Bestellung                                           |
| \_ungarischer \_ Standard sortieren      | hu-HU                                                                                               | Ungarischer Standard Reihenfolge                                           |
| \_Hungarian \_ Technical sortieren    | HU-HU- \_ technl                                                                                       | Ungarische technische Bestellung                                         |
| \_japanischen \_ radicalstroke sortieren | ja-JP                                                                                               | Japanische radikale/Stroke-Reihenfolge                                     |
| \_Japanisch ( \_ Unicode) Sortieren       | —                                                                                                   | Japanische Unicode-Bestellung **Windows 2000:** nicht unterstützt.<br/> |
| \_japanische \_ XJIS sortieren          | ja-JP                                                                                               | Japanische XJIS-Reihenfolge                                               |
| \_Koreanisch- \_ KSC sortieren             | ko-KR                                                                                               | Koreanisch (KSC)                                                  |
| \_Koreanisch- \_ Unicode sortieren         | —                                                                                                   | Koreanische Unicode-Bestellung **Windows 2000:** nicht unterstützt.<br/>   |



 

 

 




