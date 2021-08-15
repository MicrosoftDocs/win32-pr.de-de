---
description: Die folgenden Funktionen werden mit Netzwerk-DDE verwendet.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: DDE-Netzwerkfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b37e83dd6b335e1acd2e77010fa61d0da5e3e26af5b46eef54d5ee20cf2eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756309"
---
# <a name="network-dde-functions"></a>DDE-Netzwerkfunktionen

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

Die folgenden Funktionen werden mit Netzwerk-DDE verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**NDdeGetErrorString**](nddegeterrorstring.md)           | Konvertiert einen Fehlercode, der von einer Netzwerk-DDE-Funktion zurückgegeben wird, in eine Fehlerzeichenfolge, die den zurückgegebenen Fehlercode erläutert. |
| [**NDdeGetShareSecurity**](nddegetsharesecurity.md)       | Ruft den Sicherheitsdeskriptor ab, der der DDE-Freigabe zugeordnet ist.                                                      |
| [**NDdeGetTrustedShare**](nddegettrustedshare.md)         | Ruft die Optionen ab, die einer DDE-Freigabe zugeordnet sind, die sich in der Liste der vertrauenswürdigen Freigaben des Serverbenutzers befindet.                |
| [**NDdeIsValidAppTopicList**](nddeisvalidapptopiclist.md) | Bestimmt, ob eine Anwendungs- und Themenzeichenfolge ("*AppName* \| *TopicName*") die richtige Syntax verwendet.                 |
| [**NDdeIsValidShareName**](nddeisvalidsharename.md)       | Bestimmt, ob ein Freigabename die richtige Syntax verwendet.                                                               |
| [**NDdeSetShareSecurity**](nddesetsharesecurity.md)       | Legt den Sicherheitsdeskriptor fest, der der DDE-Freigabe zugeordnet ist.                                                           |
| [**NDdeSetTrustedShare**](nddesettrustedshare.md)         | Gewährt dem angegebenen DDE-Freigabe-vertrauenswürdigen Status im Kontext des aktuellen Benutzers.                                      |
| [**NDdeShareAdd**](nddeshareadd.md)                       | Erstellt eine neue DDE-Freigabe und fügt sie dem DDE-Freigabedatenbank-Manager (DSDM) hinzu.                                            |
| [**NDdeShareDel**](nddesharedel.md)                       | Löscht eine DDE-Freigabe aus dem DSDM.                                                                                    |
| [**NDdeShareEnum**](nddeshareenum.md)                     | Ruft die Liste der verfügbaren DDE-Freigaben ab.                                                                           |
| [**NDdeShareGetInfo**](nddesharegetinfo.md)               | Ruft DDE-Freigabeinformationen ab.                                                                                      |
| [**NDdeShareSetInfo**](nddesharesetinfo.md)               | Legt DDE-Freigabeinformationen fest.                                                                                           |
| [**NDdeTrustedShareEnum**](nddetrustedshareenum.md)       | Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.                 |



 

 

 



