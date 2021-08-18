---
description: Steuerungscodes, die mit Dateikomprimierung und -dekomprimierung sowie mit Wiederholungspunkten verwendet werden.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Steuerungscodes für die Verzeichnisverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1354d1a4ce72f2867ece1f15218d9c7cb3f364a12ea3eb0d3b16f66b0954e89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755190"
---
# <a name="directory-management-control-codes"></a>Steuerungscodes für die Verzeichnisverwaltung

Die folgenden Steuerungscodes werden mit [Dateikomprimierung und Dekomprimierung](file-compression-and-decompression.md)verwendet.



| Steuerungscode                                             | Bedeutung                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ GET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Ruft den aktuellen Komprimierungsstatus einer Datei oder eines Verzeichnisses auf einem Volume ab, dessen Dateisystem die Stream-bezogene Komprimierung unterstützt.<br/>    |
| [**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Legt den Komprimierungsstatus einer Datei oder eines Verzeichnisses auf einem Volume fest, dessen Dateisystem die Komprimierung pro Datei und Verzeichnis unterstützt.<br/> |



 

Die folgenden Steuerungscodes werden mit [Denkpunkten](reparse-points.md)verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Steuerungscode                                                                   | Beschreibung                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ DELETE \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Löscht einen Replikationspunkt aus der angegebenen Datei oder dem angegebenen Verzeichnis.<br/>                                              |
| [**FSCTL \_ GET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Ruft die Replikationspunktdaten ab, die der Datei oder dem Verzeichnis zugeordnet sind, die bzw. das durch das angegebene Handle identifiziert wird.<br/> |
| [**FSCTL \_ SET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Legt einen Wiederholungspunkt für eine Datei oder ein Verzeichnis fest.<br/>                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltungs-Steuerungscodes](file-management-control-codes.md)
</dt> <dt>

[Volumeverwaltungs-Steuerungscodes](volume-management-control-codes.md)
</dt> </dl>

 

