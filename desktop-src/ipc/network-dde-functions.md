---
description: Die folgenden Funktionen werden mit Network DDE verwendet.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Network DDE-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373376"
---
# <a name="network-dde-functions"></a>Network DDE-Funktionen

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Die folgenden Funktionen werden mit Network DDE verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**Ndaufgeterrorstring**](nddegeterrorstring.md)           | Konvertiert einen Fehlercode, der von einer Network DDE-Funktion zurückgegeben wird, in eine Fehler Zeichenfolge, die den zurückgegebenen Fehlercode |
| [**Ndde GetShareSecurity**](nddegetsharesecurity.md)       | Ruft die Sicherheits Beschreibung ab, die der DDE-Freigabe zugeordnet ist.                                                      |
| [**Ndbegettrustedshare**](nddegettrustedshare.md)         | Ruft die einer DDE-Freigabe zugeordneten Optionen ab, die sich in der Liste der vertrauenswürdigen Freigaben des Server Benutzers befinden.                |
| [**Nddeisvalidapptopiclist**](nddeisvalidapptopiclist.md) | Bestimmt, ob eine Anwendung und eine Themen Zeichenfolge ("*appname* \| *TopicName*") die richtige Syntax verwendet.                 |
| [**Nddeisvalidsharename**](nddeisvalidsharename.md)       | Bestimmt, ob ein Freigabe Name die richtige Syntax verwendet.                                                               |
| [**Ndde setsharesecurity**](nddesetsharesecurity.md)       | Legt die Sicherheits Beschreibung fest, die der DDE-Freigabe zugeordnet ist.                                                           |
| [**Ndabsettrustedshare**](nddesettrustedshare.md)         | Gewährt der angegebenen DDE-Freigabe den vertrauenswürdigen Status im Kontext des aktuellen Benutzers.                                      |
| [**Ndabshareadd**](nddeshareadd.md)                       | Erstellt eine neue DDE-Freigabe und fügt Sie dem DDE-Freigabe Datenbank-Manager (DSDM) hinzu.                                            |
| [**Ndde sharedel**](nddesharedel.md)                       | Löscht eine DDE-Freigabe aus dem DSDM.                                                                                    |
| [**Ndde shareerum**](nddeshareenum.md)                     | Ruft die Liste der verfügbaren DDE-Freigaben ab.                                                                           |
| [**Ndde sharegetinfo**](nddesharegetinfo.md)               | Ruft DDE-Freigabe Informationen ab.                                                                                      |
| [**Nddesharesetinfo**](nddesharesetinfo.md)               | Legt DDE-Freigabe Informationen fest.                                                                                           |
| [**Nddebug-sharede**](nddetrustedshareenum.md)       | Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.                 |



 

 

 



