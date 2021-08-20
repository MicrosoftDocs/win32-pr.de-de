---
title: Entwickeln von Anwendungen für frühere Versionen Windows
description: Erläutert, wie Sie Anwendungen entwickeln, die unter früheren Versionen von Windows ausgeführt werden, und die Vorteile der API nutzen, die mit dem Plattformupdate für Windows Vista und dem Plattformupdate für Windows Server 2008 unterstützt werden.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afbb999faf934ae621f80a824eca0289ff3df705ed11d7cfd161935c944947f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549480"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Entwickeln von Anwendungen für frühere Versionen Windows

Erläutert, wie Sie Anwendungen entwickeln, die unter früheren Versionen von Windows ausgeführt werden, und die Vorteile der API nutzen, die mit dem Plattformupdate für Windows Vista und dem Plattformupdate für Windows Server 2008 unterstützt werden.

## <a name="required-downloads"></a>Erforderliche Downloads

Das Herunterladen und Installieren der in den folgenden Abschnitten beschriebenen Pakete ist erforderlich, wenn Sie Anwendungen entwickeln möchten, die die API verwenden, die mit dem Microsoft Windows Software Development Kit (SDK) für Windows 7 eingeführt wurden.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

Das Windows SDK für Windows 7 ist zum Erstellen von Anwendungen erforderlich, die APIs verwenden, die mit dem Plattformupdate für Windows Vista und dem Plattformupdate für Windows Server 2008 unterstützt werden.

Zugriff auf zusätzliche Ressourcen und Informationen wie Downloads, Forumsbeiträge und den Blog des Windows SDK-Teams finden Sie im Windows [SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

Das .NET Framework 3.5 Service Pack 1 ist zum Erstellen von Anwendungen erforderlich, die APIs verwenden, die vom Plattformupdate für Windows Vista und dem Plattformupdate für Windows Server 2008 unterstützt werden.

Weitere Ressourcen und Informationen finden Sie im [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>DirectX SDK erforderlich bei Verwendung von Direct3D

Wenn Sie Anwendungen erstellen, die Direct3D verwenden, ist das [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( erforderlich, um Anwendungen zu erstellen, die apIs verwenden, die vom Plattformupdate für Windows Vista und dem Plattformupdate für https://msdn.microsoft.com/directx/aa937788.aspx) Windows Server 2008 unterstützt werden.

### <a name="update-your-development-computer"></a>Aktualisieren des Entwicklungscomputers

Stellen Sie sicher, dass ihr Entwicklungscomputer über alle neuesten Updates von Windows Update verfügt.

Wenn Sie Anwendungen auf einer früheren Version von Windows entwickeln, müssen Sie das Plattformupdate für Windows Vista oder das Plattformupdate für das Windows Server 2008-Update von Windows Update abrufen. Wenn Sie eines dieser Updates installieren, können Sie die neue API nutzen, die vom Windows SDK für Windows 7 bereitgestellt wird.

Weitere Informationen zum Abrufen von Updates von Windows Update finden Sie im Knowledge Base-Artikel zum Plattformupdate für [Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Entwicklungsumgebung

### <a name="set-the-build-target-to-windows-7"></a>Legen Sie build target (Buildziel) auf Windows 7 fest.

Alle Anwendungen, die Bibliotheken im Plattformupdate für Windows Vista verwenden, müssen auf der Windows 7-Zielplattform erstellt werden.

Wenn Sie WINVER auf den Windows 7-Zielplattformwert festlegen, können Sie Anwendungen entwickeln, die APIs verwenden, die mit dem Plattformupdate für Windows Vista oder dem Plattformupdate für Windows Server 2008 auf einem Entwicklungscomputer mit Windows Vista unterstützt werden.

Sie können die Zielplattform auf Windows 7 festlegen, entweder im Quellcode oder mithilfe der Option /D mit dem Visual Studio Compiler.

Das folgende Beispiel zeigt, wie WinVER in Ihrem Quellcode festgelegt wird.


```C++
#define WINVER 0x0601
```



Das folgende Beispiel zeigt, wie WINVER mithilfe der Compileroption /D festgelegt wird.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Anwendungsbereitstellung

Wenn Sie Ihre Anwendung mithilfe der Header und Bibliotheken erstellen, die vom Windows SDK für Windows 7 bereitgestellt werden, werden unterstützte APIs auf jeder Windows-Version ausgeführt, auf der das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 installiert ist.

> [!Note]  
> Das Verhalten, die Leistung oder die Anforderungen für einige APIs, die mit dem Plattformupdate für Windows Vista oder dem Plattformupdate für Windows Server 2008 unterstützt werden, können in verschiedenen Versionen von Windows. Weitere Informationen zu einer bestimmten API, die von den Updates unterstützt wird, finden Sie unter Informationen zum [Plattformupdate für Windows Vista.](platform-update-for-windows-vista-overview.md)

 

### <a name="no-redistributable-components"></a>Keine verteilbaren Komponenten

Ihre Anwendung muss keine verteilbaren Komponenten wie DLLs oder andere Laufzeitdateien installieren.

### <a name="requires-updated-end-user-computer"></a>Erfordert einen aktualisierten End-User Computer

Da das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 von Windows Update gehostet werden, verfügen Endbenutzer mit aktivierten automatischen Updates mit hoher Wahrscheinlichkeit bereits über diese Updates sowie die erforderlichen Service Packs.

Wenn auf dem Computer des Endbenutzers weder das Plattformupdate für Windows Vista noch das Plattformupdate für Windows Server 2008 installiert ist und Ihre Anwendung APIs erfordert, die mit diesen Updates unterstützt werden, kann Ihre Anwendung möglicherweise nicht auf dem Computer des Endbenutzers ausgeführt werden, oder während der Ausführung können Fehler auftreten.

Um probleme zu vermeiden, die durch veraltete Computer Ihres Benutzers verursacht werden können, sollten Sie überprüfen, ob der Computer Des Benutzers während der Installation Ihrer Anwendung über das Plattformupdate für Windows Vista oder das Plattformupdate für Windows Server 2008 verfügt. Sie können die Windows [Update-Agent-API](/windows/desktop/Wua_Sdk/portal-client) verwenden, um den Computer Ihres Endbenutzers auf installierte Updates zu überprüfen. Sie können auch die Windows Update-Agent-API verwenden, um erforderliche Updates während der Anwendungsinstallation herunterzuladen und zu installieren, wenn der Endbenutzer die Updates noch nicht installiert hat.

Ein Beispiel für ein Installationsprogramm, das die Verwendung der [Windows Update Agent-API](/windows/desktop/Wua_Sdk/portal-client)veranschaulicht, finden Sie unter [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) im [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Obwohl das Beispiel für das Installationsprogramm D3D11InstallHelper, das unter [Direct3D 11 Deployment for Game Developers (Direct3D 11-Bereitstellung](../direct3darticles/direct3d11-deployment.md)für Spieleentwickler) erläutert wird, für Anwendungen geschrieben wurde, die Direct3D 11 verwenden, bietet es ein gutes Beispiel für die Interaktion mit der [Windows Update-Agent-API,](/windows/desktop/Wua_Sdk/portal-client) um den Download und die Installation von Updates zu initiieren und zu verfolgen, die von Windows Update gehostet werden. Zum Kompilieren dieses Beispiels ist möglicherweise das Windows SDK für Windows 7 erforderlich. Weitere Informationen zum Beispiel D3D11InstallHelper, einschließlich bekannter Probleme, finden Sie im [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( Versionshinweise für https://msdn.microsoft.com/directx/aa937788.aspx) August 2009.Plattformupdate für Windows Vista)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plattformupdate für Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Übersichten**
</dt> <dt>

[Informationen zum Plattformupdate für Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base Artikel zum Plattformupdate für Windows Vista (KB-971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 