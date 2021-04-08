---
description: Steuerungs Codes, die mit Dateikomprimierung und Dekomprimierung und mit Analyse Punkten verwendet werden.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Steuerungs Codes für die Verzeichnis Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867695"
---
# <a name="directory-management-control-codes"></a>Steuerungs Codes für die Verzeichnis Verwaltung

Die folgenden Steuerungs Codes werden bei der [Dateikomprimierung und-Dekomprimierung](file-compression-and-decompression.md)verwendet.



| Steuerungscode                                             | Bedeutung                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Komprimierung von "f" \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Ruft den aktuellen Komprimierungs Status einer Datei oder eines Verzeichnisses auf einem Volume ab, dessen Dateisystem die Komprimierung pro Stream unterstützt.<br/>    |
| [**Komprimierung von ssctl- \_ Satz \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Legt den Komprimierungs Status einer Datei oder eines Verzeichnisses auf einem Volume fest, dessen Dateisystem die Komprimierung pro Datei und pro Verzeichnis unterstützt.<br/> |



 

Die folgenden Steuerungs Codes werden mit Analyse [Punkten](reparse-points.md)verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Steuerungscode                                                                   | BESCHREIBUNG                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**Lösch Analyse Punkt für den \_ Löschvorgang \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Löscht einen Analyse Punkt aus der angegebenen Datei bzw. dem angegebenen Verzeichnis.<br/>                                              |
| [**Sicherungspunkt für "f" \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Ruft die Analyse Punktdaten ab, die der Datei oder dem Verzeichnis zugeordnet sind, die durch das angegebene Handle identifiziert werden.<br/> |
| [**Analyse Punkt für die ssctl- \_ Gruppe \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Legt einen Analyse Punkt für eine Datei oder ein Verzeichnis fest.<br/>                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateiverwaltungs-Steuerungscodes](file-management-control-codes.md)
</dt> <dt>

[Volumeverwaltungs-Steuerungscodes](volume-management-control-codes.md)
</dt> </dl>

 

