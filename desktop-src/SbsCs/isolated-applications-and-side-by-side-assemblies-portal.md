---
description: Verwalten Sie die assemblyfreigabe und die dll-Versionsverwaltung im nebeneinander gespeicherten Assemblyspeicher über Programme. Schreiben von Assemblymanifesten und selbst beschreibenden Anwendungen für das Freigeben und Umleiten von DLLs.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Isolierte Anwendungen und parallele Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128821"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Isolierte Anwendungen und parallele Assemblys

## <a name="purpose"></a>Zweck

Isolierte Anwendungen und parallele Assemblys sind eine Microsoft Windows-Lösung, mit der die Versions Konflikte in Windows-Client Anwendungen verringert werden. Mit Windows können Anwendungsentwickler isolierte Anwendungen erstellen, die vollständig selbst beschreibend sind und von Änderungen an der Registrierung, anderen Anwendungen oder anderen Versionen von Assemblys, die auf dem System ausgeführt werden, nicht betroffen sind. Anwendungs Autoren und Administratoren können Manifeste verwenden, um die Freigabe von parallelen Assemblys nach der Bereitstellung entweder auf globaler oder pro Anwendung zu verwalten. Kunden profitieren von isolierten Anwendungen, die stabiler und zuverlässiger aktualisiert werden.

## <a name="where-applicable"></a>Anwendungsbereich

Isolierte Anwendungen und parallele assemblyfreigabe können verwendet werden, um Anwendungen zu entwickeln, die Betriebs Systemassemblys sicher freigeben. Entwickler können diese Technologie verwenden, um dll-Versions Verwaltungs Konflikte zu beheben, die durch eine nicht kompatible Version einer freigegebenen Assembly verursacht werden.

Wenn Ihre Anwendung die Version einer Komponente, die Sie getestet haben, konsistent finden muss, ist es möglich, die Anwendung so zu isolieren, dass Sie immer mit der getesteten Version der Komponente auf dem Computer des Benutzers ausgeführt wird.

Isolierte Anwendungen und parallele Assemblys sind für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Dokumentation richtet sich hauptsächlich an Softwareentwickler, Anwendungsentwickler und Netzwerkadministratoren:

-   Software Entwickler, die isolierte Anwendungen erstellen möchten, die die parallelen Assemblys verwenden, die von Microsoft und anderen parallelen assemblyverlegern zur Verfügung gestellt werden.
-   Anwendungsentwickler, die daran interessiert sind, eigene parallele Assemblys zu erstellen, um Ihre Anwendungen zu isolieren.
-   Netzwerkadministratoren, die weitere Informationen zu isolierten Anwendungen benötigen.

In dieser Dokumentation finden Sie als Haupt Referenz für parallele assemblyfreigabe und isolierte Anwendungen allgemeine Hintergrundinformationen zum Erstellen von Manifesten und parallelen Assemblys, zum Installieren von isolierten Anwendungen und parallelen Assemblys sowie zur Verwendung der Aktivierungs Kontext-API.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Windows Server 2003 und höher oder Windows XP und höher müssen parallele Assemblys und Manifeste verwenden, um Anwendungen zu isolieren und die Aktivierungs Kontext-API zu verwenden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                         | BESCHREIBUNG                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Verweis](side-by-side-assemblies-reference.md)<br/> | Dokumentation zu isolierten Anwendungen und parallelen Assemblys.<br/> |



 

 

 




