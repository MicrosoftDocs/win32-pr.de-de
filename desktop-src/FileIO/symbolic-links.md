---
description: Eine symbolische Verknüpfung ist ein Dateisystem Objekt, das auf ein anderes Dateisystem Objekt zeigt. Das Objekt, auf das verwiesen wird, wird als Ziel bezeichnet.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Symbolische Links
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352260"
---
# <a name="symbolic-links"></a>Symbolische Links

Eine symbolische Verknüpfung ist ein Dateisystem Objekt, das auf ein anderes Dateisystem Objekt zeigt. Das Objekt, auf das verwiesen wird, wird als Ziel bezeichnet.

Symbolische Verknüpfungen sind für Benutzer transparent. die Links werden als normale Dateien oder Verzeichnisse angezeigt und können vom Benutzer oder der Anwendung auf die gleiche Weise bearbeitet werden.

Symbolische Verknüpfungen sollen die Migration und Anwendungskompatibilität mit UNIX-Betriebssystemen erleichtern. Microsoft hat seine symbolischen Verknüpfungen so implementiert, dass Sie genau wie Unix-Links funktionieren.

Weitere Informationen finden Sie in den nachfolgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | BESCHREIBUNG                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Symbolische Verknüpfungs Effekte in Dateisystemfunktionen](symbolic-link-effects-on-file-systems-functions.md)<br/> | Funktionsweise von symbolischen Verknüpfungen auf Standarddatei Funktionen, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben.<br/>                                        |
| [Überlegungen zur Programmierung](symbolic-link-programming-considerations.md)<br/>                             | Programmier Überlegungen für die Arbeit mit symbolischen Verknüpfungen.<br/>                                                                                |
| [Erstellen von symbolischen Verknüpfungen](creating-symbolic-links.md)<br/>                                                 | Erstellen Sie symbolische Verknüpfungen, die einen absoluten oder relativen Pfad verwenden, indem Sie die Funktion " [**kreatesymboliclink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) " verwenden.<br/> |



 

## <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

Symbolische Verknüpfungen stehen in NTFS ab Windows Vista zur Verfügung.

 

 




