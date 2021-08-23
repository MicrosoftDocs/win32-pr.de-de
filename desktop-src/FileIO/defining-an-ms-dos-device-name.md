---
description: Ein MS-DOS-Gerätename ist eine Verbindung, die auf den Pfad eines MS-DOS-Geräts verweist. Diese Verbindungen bilden den MS-DOS-Gerätenamespace.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definieren eines MS-DOS-Gerätenamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77331c1d3b3cc7566f118fa19fbb13c84e82af634f1098193bdf3dcb6270ef7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638930"
---
# <a name="defining-an-ms-dos-device-name"></a>Definieren eines MS-DOS-Gerätenamens

Ein MS-DOS-Gerätename ist eine Verbindung, die auf den Pfad eines MS-DOS-Geräts verweist. Diese Verbindungen bilden den MS-DOS-Gerätenamespace. Rufen Sie die Funktionen [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) und [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) auf, um diese Verbindungen zu erstellen und zu ändern. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) löscht eine verbindung, die von **SetVolumeMountPoint** erstellt wurde, und **DefineDosDevice** löscht die erstellten Verbindungen.

Nachdem ein MS-DOS-Gerätename definiert wurde, bleibt er für alle Prozesse sichtbar.

-   Alle MS-DOS-Geräte werden durch Windows über eine Authentifizierungs-ID identifiziert. Eine Authentifizierungs-ID ist die LUID (lokal eindeutiger Bezeichner), die bei der Erstellung jeder Anmeldesitzung zugeordnet ist.
-   Die Sichtbarkeit eines MS-DOS-Gerätenamens wird entweder als global oder lokal kategorisiert und als solche definiert, indem er in die namespaces "Globales MS-DOS-Gerät" und "Lokales MS-DOS-Gerät" aufgenommen wird. Auf den Inhalt von MS-DOS-Geräten im globalen Namespace kann von allen Benutzern zugegriffen werden, und auf den Inhalt von MS-DOS-Geräten im lokalen Namespace kann nur der Benutzer zugreifen, dessen Zugriffstoken die Authentifizierungs-ID enthält, die diesem lokalen MS-DOS-Gerätenamespace zugeordnet ist.

Mehrere lokale MS-DOS-Gerätenamespaces und nur ein globaler MS-DOS-Gerätenamespace können gleichzeitig und auf einem Computer vorhanden sein.

Beachten Sie, dass nur Prozesse, die im LocalSystem-Kontext ausgeführt werden, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) aufrufen können, um ein MS-DOS-Gerät im globalen MS-DOS-Gerätenamespace zu erstellen. Außerdem wird der lokale MS-DOS-Gerätenamespace, der einer bestimmten AuthenticationID entspricht, gelöscht, wenn der letzte Verweis auf diese AuthenticationID entfernt wird.

Wenn Ihr Code einen vorhandenen MS-DOS-Gerätenamen durch Aufrufen von [**QueryDosDevice abfragt,**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)wird zunächst der Namespace Lokales MS-DOS-Gerät durchsucht. Wenn sie dort nicht gefunden wird, durchsucht die Funktion den globalen MS-DOS-Gerätenamespace. Wenn Ihr Code alle vorhandenen MS-DOS-Gerätenamen über diese Funktion abfragt, hängt die Liste der zurückgegebenen Namen davon ab, ob sie im LocalSystem-Kontext ausgeführt wird. Wenn ja, werden nur die MS-DOS-Gerätenamen zurückgegeben, die im globalen MS-DOS-Gerätenamespace enthalten sind. Andernfalls wird eine Verkettung der Gerätenamen im globalen und lokalen MS-DOS-Gerätenamespace zurückgegeben. Wenn in beiden Namespaces ein Gerätename vorhanden ist, gibt **QueryDosDevice** den Eintrag im Namespace Lokales MS-DOS-Gerät zurück. Dies gilt auch für die Liste aller MS-DOS-Gerätenamen, die von [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) und [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)zurückgegeben werden.

Beachten Sie, dass das folgende Szenario auftreten kann:

1.  Benutzer A, der nicht im LocalSystem-Kontext ausgeführt wird, erstellt einen Gerätenamen im entsprechenden Lokalen MS-DOS-Gerätenamespace, und dieser Gerätename ist im globalen MS-DOS-Gerätenamespace nicht vorhanden.
2.  Benutzer B, der im LocalSystem-Kontext ausgeführt wird, erstellt den gleichen Gerätenamen im globalen MS-DOS-Gerätenamespace.

In diesem Szenario hat Benutzer A erst Dann Zugriff auf den Gerätenamen im globalen MS-DOS-Gerätenamespace, wenn er den Gerätenamen in seinem lokalen MS-DOS-Gerätenamespace entfernt oder umbenennt. Um die Wahrscheinlichkeit zu verringern, dass dieses Szenario eintritt, sollten MS-DOS-Laufwerkbuchstaben im globalen MS-DOS-Gerätenamespace zugeordnet werden, beginnend mit C: und endend mit Z:. Diese Sequenz sollte für die Zuordnung von MS-DOS-Laufwerkbuchstaben im Namespace Lokales MS-DOS-Gerät umgekehrt werden.

Wenn Sie nicht innerhalb des LocalSystem-Kontexts ausführen, können Sie mit [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) keinen Gerätenamen im Namespace Lokales MS-DOS-Gerät definieren, wenn dieser Gerätename bereits in Ihren lokalen oder globalen MS-DOS-Gerätenamespaces vorhanden ist. Rufen Sie [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) auf, bevor **Sie DefineDosDevice** aufrufen, um zu bestimmen, ob der Gerätename, den Sie definieren möchten, in Ihren MS-DOS-Gerätenamespaces vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



