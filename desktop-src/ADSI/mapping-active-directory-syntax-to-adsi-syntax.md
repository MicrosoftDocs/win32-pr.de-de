---
title: Zuordnung Active Directory Syntax zur ADSI-Syntax
description: In der folgenden Tabelle sind die Active Directory Syntaxen der entsprechenden ADSI-Syntax zugeordnet.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- Attribute ADSI, Mapping Active Directory Syntax zur ADSI-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340605"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Zuordnung Active Directory Syntax zur ADSI-Syntax

In der folgenden Tabelle sind die Active Directory Syntaxen der entsprechenden ADSI-Syntax zugeordnet.



| Attribut Syntax-ID | Active Directory-Syntax Typs             | Äquivalente ADSI-Syntax Typen                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | DN-Zeichenfolge<br/>                     | DN-Zeichenfolge<br/>                                                |
| 2.5.5.2<br/>  | ObjectID<br/>                     | Caseignore-Zeichenfolge<br/>                                        |
| 2.5.5.3<br/>  | Groß-/Kleinschreibung<br/>         | Caseexact-Zeichenfolge<br/>                                         |
| 2.5.5.4<br/>  | Case-Zeichenfolge ignoriert<br/>           | Caseignore-Zeichenfolge<br/>                                        |
| 2.5.5.5<br/>  | Print Case-Zeichenfolge<br/>             | Druckbare Zeichenfolge<br/>                                         |
| 2.5.5.6<br/>  | Numerische Zeichenfolge<br/>                | Numerische Zeichenfolge<br/>                                           |
| 2.5.5.7<br/>  | **Oder** Name dnwithoctetstring<br/> | Nicht unterstützt<br/>                                            |
| 2.5.5.8<br/>  | Boolean<br/>                       | Boolean<br/>                                                  |
| 2.5.5.9<br/>  | Integer<br/>                       | Integer<br/>                                                  |
| 2.5.5.10<br/> | Oktett-Zeichenfolge<br/>                  | Oktett-Zeichenfolge<br/>                                             |
| 2.5.5.11<br/> | Time<br/>                          | UTC-Zeit<br/>                                                 |
| 2.5.5.12<br/> | Unicode<br/>                       | Case-Zeichenfolge ignorieren<br/>                                       |
| 2.5.5.13<br/> | Adresse<br/>                       | Nicht unterstützt<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | NT-Sicherheits Beschreibung<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Große ganze Zahl<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Oktett-Zeichenfolge<br/>                                             |



 

 

 





