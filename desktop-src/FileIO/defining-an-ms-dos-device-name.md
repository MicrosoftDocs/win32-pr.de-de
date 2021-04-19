---
description: Ein MS-DOS-Gerätename ist eine Verknüpfung, die auf den Pfad eines MS-DOS-Geräts zeigt. Diese Verbindungen bilden den MS-DOS-Geräte Namespace.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definieren eines MS-DOS-Geräte namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed89e1d9938e320ecce3ff0b35b8ae0792fe219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349129"
---
# <a name="defining-an-ms-dos-device-name"></a>Definieren eines MS-DOS-Geräte namens

Ein MS-DOS-Gerätename ist eine Verknüpfung, die auf den Pfad eines MS-DOS-Geräts zeigt. Diese Verbindungen bilden den MS-DOS-Geräte Namespace. Rufen Sie die Funktionen [**definedosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) und [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) auf, um diese Verbindungen zu erstellen und zu ändern. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) löscht eine von **setvolumemountpoint** erstellte Verknüpfung, und **definedosdevice** löscht die von ihm erstellten Verbindungen.

Nachdem ein MS-DOS-Gerätename definiert wurde, bleibt er für alle Prozesse sichtbar.

-   Alle MS-DOS-Geräte werden von Windows über eine Authentifizierungs-ID identifiziert. Eine Authentifizierungs-ID ist die LUID (lokal eindeutiger Bezeichner), die jeder Anmelde Sitzung zugeordnet ist, wenn Sie erstellt wird.
-   Die Sichtbarkeit eines MS-DOS-Geräte namens wird entweder global oder local kategorisiert und ist so definiert, dass er in das globale MS-DOS-Gerät und die lokalen MS-DOS-Geräte Namespaces eingeschlossen wird. Der Zugriff auf den Inhalt der MS-DOS-Geräte im globalen Namespace kann von allen Benutzern erfolgen, und auf den Inhalt von MS-DOS-Geräten im lokalen Namespace kann nur von dem Benutzer zugegriffen werden, dessen Zugriffs Token die authenticationid enthält, die diesem lokalen MS-DOS-Geräte Namespace zugeordnet ist.

Es können mehrere lokale MS-DOS-Geräte-Namespaces und nur ein globaler MS-DOS-Geräte Namespace gleichzeitig und auf einem Computer vorhanden sein.

Beachten Sie, dass nur Prozesse, die im LocalSystem-Kontext ausgeführt werden, [**definedosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) aufgerufen werden können, um im globalen MS-DOS-Geräte Namespace ein MS-DOS-Gerät zu erstellen. Außerdem wird der lokale MS-DOS-Geräte Namespace, der einer bestimmten authenticationid entspricht, gelöscht, wenn der letzte Verweis auf diese authenticationid entfernt wird.

Wenn Ihr Code einen vorhandenen MS-DOS-Gerätenamen durch Aufrufen von [**querydosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew)abfragt, wird zuerst der lokale MS-DOS-Geräte Namespace durchsucht. Wenn Sie dort nicht gefunden wird, durchsucht die Funktion den globalen MS-DOS-Geräte-Namespace. Wenn Ihr Code alle vorhandenen MS-DOS-Gerätenamen über diese Funktion abfragt, ist die Liste der zurückgegebenen Namen davon abhängig, ob Sie im LocalSystem-Kontext ausgeführt wird. Wenn dies der Fall ist, werden nur die MS-DOS-Gerätenamen zurückgegeben, die im globalen MS-DOS-Geräte Namespace enthalten sind Wenn dies nicht der Fall ist, wird eine Verkettung der Gerätenamen in den globalen und lokalen MS-DOS-gerätenamespaces zurückgegeben. Wenn ein Gerätename in beiden Namespaces vorhanden ist, gibt **querydosdevice** den Eintrag im Namespace des lokalen MS-DOS-Geräts zurück. Dies gilt auch für die Liste aller von [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) und [**getlogicaldrivestrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)zurückgegebenen MS-DOS-Gerätenamen.

Beachten Sie, dass das folgende Szenario auftreten kann:

1.  Benutzer A, der nicht im LocalSystem-Kontext ausgeführt wird, erstellt einen Gerätenamen im entsprechenden lokalen MS-DOS-Geräte Namespace, und der Gerätename ist im globalen MS-DOS-Geräte Namespace nicht vorhanden.
2.  Benutzer B, der innerhalb des LocalSystem-Kontexts ausgeführt wird, erstellt denselben Gerätenamen im globalen MS-DOS-Geräte Namespace.

In diesem Szenario hat Benutzer A keinen Zugriff auf den Gerätenamen im globalen MS-DOS-Geräte Namespace, bis er den Gerätenamen in seinem lokalen MS-DOS-Geräte Namespace entfernt oder umbenennt. Um die Wahrscheinlichkeit des Auftretens dieses Szenarios zu reduzieren, sollten Sie MS-DOS-Laufwerk Buchstaben im globalen MS-DOS-Geräte Namespace zuordnen, beginnend mit "C:" und "z:". Diese Sequenz sollte für die Zuordnung von MS-DOS-Laufwerk Buchstaben im lokalen MS-DOS-Geräte-Namespace umgekehrt werden.

Wenn Sie nicht im LocalSystem-Kontext ausgeführt werden, können Sie mit [**definedosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) keinen Gerätenamen im lokalen MS-DOS-Geräte Namespace definieren, wenn dieser Gerätename bereits in Ihren lokalen oder globalen MS-DOS-Geräte Namespaces vorhanden ist. Rufen Sie [**querydosdevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) auf, bevor Sie **definedosdevice** aufrufen, um zu bestimmen, ob der zu definierenden Gerätename in den MS-DOS-Geräte Namespaces vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



