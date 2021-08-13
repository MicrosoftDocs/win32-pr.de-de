---
description: Die Aktion RegisterTypeLibraries registriert Typbibliotheken beim System. Diese Aktion wird auf jede Datei angewendet, auf die in der TypeLib-Tabelle verwiesen wird, die für die Installation geplant ist.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: RegisterTypeLibraries-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac42c831c8413f297d3df2302523a2372b11d1efcffe82ce0d3a82da722832cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626763"
---
# <a name="registertypelibraries-action"></a>RegisterTypeLibraries-Aktion

Die Aktion RegisterTypeLibraries registriert Typbibliotheken beim System. Diese Aktion wird auf jede Datei angewendet, auf die in der [TypeLib-Tabelle](typelib-table.md) verwiesen wird, die für die Installation geplant ist.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Aktion RegisterTypeLibraries muss nach der [Aktion InstallFiles angegeben](installfiles-action.md) werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) der registrierten Typbibliothek. |



 

## <a name="remarks"></a>Hinweise

Die Aktion RegisterTypeLibraries erfordert, dass die Typbibliothekssprache im Feld Sprache der TypeLib-Tabelle ordnungsgemäß geschrieben wird. Eine falsche Erstellung des Felds Sprache kann dazu führen, dass das Installationsprogramm keine ansonsten gültige Typbibliothek registriert.

 

 



