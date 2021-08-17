---
description: Eine symbolische Verknüpfung ist ein Dateisystemobjekt, das auf ein anderes Dateisystemobjekt verweist. Das Objekt, auf das gezeigt wird, wird als Ziel bezeichnet.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Symbolische Links
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126897dc230b36f504ef17653daea32b1076d10870a3a22015462f3abec05448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951029"
---
# <a name="symbolic-links"></a>Symbolische Links

Eine symbolische Verknüpfung ist ein Dateisystemobjekt, das auf ein anderes Dateisystemobjekt verweist. Das Objekt, auf das gezeigt wird, wird als Ziel bezeichnet.

Symbolische Verknüpfungen sind für Benutzer transparent. Die Links werden als normale Dateien oder Verzeichnisse angezeigt und können vom Benutzer oder der Anwendung auf genau die gleiche Weise verwendet werden.

Symbolische Verknüpfungen sollen die Migration und Anwendungskompatibilität mit UNIX-Betriebssystemen erleichtern. Microsoft hat seine symbolischen Verknüpfungen zur Funktion wie UNIX-Links implementiert.

Weitere Informationen finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                             | Beschreibung                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Auswirkungen symbolischer Verknüpfungen auf Dateisystemfunktionen](symbolic-link-effects-on-file-systems-functions.md)<br/> | Auswirkungen symbolischer Verknüpfungen auf Standarddateifunktionen, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben.<br/>                                        |
| [Überlegungen zur Programmierung](symbolic-link-programming-considerations.md)<br/>                             | Überlegungen zur Programmierung bei der Arbeit mit symbolischen Verknüpfungen.<br/>                                                                                |
| [Erstellen symbolischer Verknüpfungen](creating-symbolic-links.md)<br/>                                                 | Erstellen Sie symbolische Verknüpfungen, die entweder einen absoluten oder relativen Pfad verwenden, indem Sie die [**CreateSymbolicLink-Funktion**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) verwenden.<br/> |



 

## <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

Symbolische Verknüpfungen sind ab Windows Vista in NTFS verfügbar.

 

 




