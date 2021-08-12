---
title: Zuordnen der Active Directory-Syntax zur ADSI-Syntax
description: Die folgende Tabelle ordnet die Active Directory-Syntax den entsprechenden ADSI-Syntaxen zu.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- ADSI-Attribute, Zuordnung der Active Directory-Syntax zur ADSI-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04682a1e299e14c55c520310bff697ea6664d4dabe71380f7a146fd2dfff053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179278"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Zuordnen der Active Directory-Syntax zur ADSI-Syntax

Die folgende Tabelle ordnet die Active Directory-Syntax den entsprechenden ADSI-Syntaxen zu.



| Attributsyntax-ID | Active Directory-Syntaxtyp             | Äquivalenter ADSI-Syntaxtyp                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | DN-Zeichenfolge<br/>                     | DN-Zeichenfolge<br/>                                                |
| 2.5.5.2<br/>  | Objekt-ID<br/>                     | CaseIgnore-Zeichenfolge<br/>                                        |
| 2.5.5.3<br/>  | Zeichenfolge mit Zeichenfolge mit Sensitiver Schreibung<br/>         | CaseExact String<br/>                                         |
| 2.5.5.4<br/>  | Zeichenfolge mit ignorierter Case-Zeichenfolge<br/>           | CaseIgnore-Zeichenfolge<br/>                                        |
| 2.5.5.5<br/>  | Druckfallzeichenfolge<br/>             | Druckbare Zeichenfolge<br/>                                         |
| 2.5.5.6<br/>  | Numerische Zeichenfolge<br/>                | Numerische Zeichenfolge<br/>                                           |
| 2.5.5.7<br/>  | **OR** Name DNWithOctetString<br/> | Nicht unterstützt<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Integer<br/>                       | Integer<br/>                                                  |
| 2.5.5.10<br/> | Oktettzeichenfolge<br/>                  | Oktettzeichenfolge<br/>                                             |
| 2.5.5.11<br/> | Time<br/>                          | UTC-Zeit<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Case Ignore String<br/>                                       |
| 2.5.5.13<br/> | Adresse<br/>                       | Nicht unterstützt<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | NT-Sicherheitsbeschreibung<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Große ganze Zahl<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Oktettzeichenfolge<br/>                                             |



 

 

 





