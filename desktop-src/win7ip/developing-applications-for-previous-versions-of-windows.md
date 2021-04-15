---
title: Entwickeln von Anwendungen für frühere Versionen von Windows
description: Erläutert, was Sie tun müssen, um Anwendungen zu entwickeln, die unter früheren Versionen von Windows ausgeführt werden, und die API zu nutzen, die mit dem Platt Form Update für Windows Vista und dem Platt Form Update für Windows Server 2008 unterstützt wird.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104393890"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a>Entwickeln von Anwendungen für frühere Versionen von Windows

Erläutert, was Sie tun müssen, um Anwendungen zu entwickeln, die unter früheren Versionen von Windows ausgeführt werden, und die API zu nutzen, die mit dem Platt Form Update für Windows Vista und dem Platt Form Update für Windows Server 2008 unterstützt wird.

## <a name="required-downloads"></a>Erforderliche Downloads

Das herunterladen und Installieren der in den folgenden Abschnitten beschriebenen Pakete ist erforderlich, wenn Sie Anwendungen entwickeln möchten, die API verwenden, die mit dem Microsoft Windows Software Development Kit (SDK) für Windows 7 eingeführt wurden.

### <a name="microsoft-windows-sdk"></a>Microsoft Windows SDK

Die Windows SDK für Windows 7 ist erforderlich, um Anwendungen zu erstellen, die APIs verwenden, die mit dem Platt Form Update für Windows Vista unterstützt werden, und das Platt Form Update für Windows Server 2008.

Informationen zum Zugriff auf Weitere Ressourcen und Informationen, z. b. Downloads, Forumsbeiträge und den Windows SDK Teamblog, finden Sie im [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .

### <a name="net-framework"></a>.NET Framework

Das .NET Framework 3,5 Service Pack 1 ist erforderlich, um Anwendungen zu erstellen, die APIs verwenden, die vom Platt Form Update für Windows Vista unterstützt werden, und das Platt Form Update für Windows Server 2008.

Weitere Ressourcen und Informationen finden Sie im [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) () https://msdn.microsoft.com/netframework/default.aspx) .

### <a name="directx-sdk-required-when-using-direct3d"></a>Beim Verwenden von Direct3D ist ein DirectX SDK erforderlich.

Wenn Sie Anwendungen erstellen, die Direct3D verwenden, ist das [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) erforderlich für das Erstellen von Anwendungen, die APIs verwenden, die vom Platt Form Update für Windows Vista unterstützt werden, und das Platt Form Update für Windows Server 2008.

### <a name="update-your-development-computer"></a>Aktualisieren des Entwicklungs Computers

Stellen Sie sicher, dass auf Ihrem Entwicklungs Computer alle neuesten Updates von Windows Update.

Wenn Sie Anwendungen in einer früheren Version von Windows entwickeln, müssen Sie das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008-Update von Windows Update abrufen. Wenn Sie eines dieser Updates installieren, können Sie die neue API nutzen, die von der Windows SDK für Windows 7 bereitgestellt wird.

Weitere Informationen zum Abrufen von Updates von Windows Update finden Sie im [Knowledge Base-Artikel über das Platt Form Update für Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .

## <a name="development-environment"></a>Entwicklungsumgebung

### <a name="set-the-build-target-to-windows-7"></a>Festlegen des Buildziels auf Windows 7

Alle Anwendungen, die Bibliotheken im Platt Form Update für Windows Vista verwenden, müssen für die Zielplattform von Windows 7 erstellt werden.

Durch Festlegen von WINVER auf den Windows 7-Ziel Platt Form Wert können Sie Anwendungen entwickeln, die APIs verwenden, die mit dem Platt Form Update für Windows Vista unterstützt werden, oder das Platt Form Update für Windows Server 2008 auf einem Entwicklungs Computer mit Windows Vista.

Sie können die Zielplattform auf Windows 7 festlegen, entweder im Quellcode oder mithilfe der Option/D mit dem Visual Studio-Compiler.

Im folgenden Beispiel wird gezeigt, wie Sie in Ihrem Quellcode "winver" festlegen.


```C++
#define WINVER 0x0601
```



Im folgenden Beispiel wird gezeigt, wie winver mithilfe der/D-Compileroption festgelegt wird.

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a>Anwendungsbereitstellung

Wenn Sie Ihre Anwendung mit den Headern und Bibliotheken erstellen, die von der Windows SDK für Windows 7 bereitgestellt werden, werden die unterstützten APIs unter allen Windows-Versionen ausgeführt, auf denen das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008 installiert ist.

> [!Note]  
> Das Verhalten, die Leistung oder die Anforderungen für einige APIs, die mit dem Platt Form Update für Windows Vista oder dem Platt Form Update für Windows Server 2008 unterstützt werden, können in verschiedenen Windows-Versionen variieren. Ausführliche Informationen zu einer bestimmten API, die von den Updates unterstützt wird, finden Sie unter [Informationen zum Platt Form Update für Windows Vista](platform-update-for-windows-vista-overview.md).

 

### <a name="no-redistributable-components"></a>Keine weitervertreibbaren Komponenten

Die Anwendung muss keine weitervertreibbaren Komponenten installieren, z. b. DLLs oder andere Laufzeitdateien.

### <a name="requires-updated-end-user-computer"></a>Erfordert aktualisierte End-User Computer

Da das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 von Windows Update gehostet werden, verfügen Endbenutzer mit aktivierten automatischen Updates höchstwahrscheinlich bereits über diese Updates und die erforderlichen Service Packs.

Wenn auf dem Computer des Endbenutzers kein Platt Form Update für Windows Vista oder ein Platt Form Update für Windows Server 2008 installiert ist und Ihre Anwendung APIs erfordert, die von diesen Updates unterstützt werden, kann die Anwendung möglicherweise nicht auf dem Computer des Endbenutzers ausgeführt werden, oder es kann während der Ausführung zu Fehlern kommen.

Um Probleme zu vermeiden, die möglicherweise durch einen veralteten Computer Ihres Benutzers verursacht werden, sollten Sie überprüfen, ob der Computer des Benutzers über das Platt Form Update für Windows Vista oder das Platt Form Update für Windows Server 2008-Update während der Installation der Anwendung verfügt. Mit der Windows Update- [Agent-API](/windows/desktop/Wua_Sdk/portal-client) können Sie den Computer des Endbenutzers auf installierte Updates überprüfen. Sie können auch die Windows Update-Agent-API verwenden, um erforderliche Updates während der Installation der Anwendung herunterzuladen und zu installieren, wenn die Updates nicht bereits von Endbenutzern installiert wurden.

Ein Beispiel für ein Installationsprogramm, das die Verwendung der [Windows Update-Agent-API](/windows/desktop/Wua_Sdk/portal-client)veranschaulicht, finden Sie unter [Bereitstellung von Direct3D 11 für Spieleentwickler](../direct3darticles/direct3d11-deployment.md) im [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .

Obwohl das D3D11InstallHelper Installer-Beispiel, das in der [Direct3D 11-Bereitstellung für Spieleentwickler](../direct3darticles/direct3d11-deployment.md)erläutert wird, für Anwendungen geschrieben wurde, die Direct3D 11 verwenden, bietet es ein gutes Beispiel für die Interaktion mit der [Windows Update-Agent-API](/windows/desktop/Wua_Sdk/portal-client) , um den Download und die Installation von Updates zu initiieren und zu verfolgen, die von Windows Update gehostet werden. Zum Kompilieren dieses Beispiels ist möglicherweise die Windows SDK für Windows 7 erforderlich. Weitere Informationen zum D3D11InstallHelper-Beispiel, einschließlich bekannter Probleme, finden Sie unter [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) Anmerkungen zu dieser Version von August 2009. Platt Form Update für Windows Vista).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Platt Form Update für Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Übersichten**
</dt> <dt>

[Informationen zum Platt Form Update für Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base-Artikel zum Platt Form Update für Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 