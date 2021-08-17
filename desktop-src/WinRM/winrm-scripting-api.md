---
title: WinRM-Skript-API
description: Windows Skriptobjekte für die Remoteverwaltung werden als Ebene oberhalb des WS-Management-Protokolls implementiert.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742758"
---
# <a name="winrm-scripting-api"></a>WinRM-Skript-API

Windows Skriptobjekte für die Remoteverwaltung werden als Ebene oberhalb der [WS-Management-Protokoll](ws-management-protocol.md)implementiert. Mit den Skriptobjekten können Sie Daten abrufen oder [*Ressourcen*](windows-remote-management-glossary.md) auf lokalen und Remotecomputern verwalten.

## <a name="ws-management-objects"></a>WS-Management-Objekte

Jedes Skriptobjekt verfügt über eine entsprechende C++-Schnittstelle. Weitere Informationen finden Sie unter [WinRM C++-API](winrm-c---api.md) und [Skripterstellung in Windows Remoteverwaltung.](scripting-in-windows-remote-management.md)

Die folgenden Objekte werden von der WinRM-Skripterstellungs-API bereitgestellt.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**Connectionoptions**](connectionoptions.md)
</dt> <dd>

Definiert den Benutzernamen und das Kennwort, die für Remoteverbindungen verwendet werden. Der Benutzername und das Kennwort werden beim Aufrufen der [**CreateConnectionOptions-Methode**](wsman-createconnectionoptions.md) übergeben. Weitere Informationen finden Sie unter [Abrufen von Daten von einem Remotecomputer.](obtaining-data-from-a-remote-computer.md) Die entsprechende C++-Schnittstelle ist [**IWSManConnectionOptions.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)
</dt> <dd>

Stellt eine Auflistung von Ergebnissen dar, die beim Aufzählen einer Ressource zurückgegeben werden. Weitere Informationen finden Sie unter [Auflisten oder Auflisten aller Instanzen einer Ressource.](enumerating-or-listing-all-instances-of-a-resource.md) Die entsprechende C++-Schnittstelle ist [**IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**Resourcelocator**](resourcelocator.md)
</dt> <dd>

Gibt den Pfad zu einer Ressource an. Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)verwenden. Die entsprechende C++-Schnittstelle ist [**IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sitzung**](session.md)
</dt> <dd>

Definiert die für die Sitzung verfügbaren Netzwerkvorgänge und Eigenschaften, z. B. [**Session.Get,**](session-get.md) [**Session.Enumerate,**](session-enumerate.md) [**Session.Invoke.**](session-invoke.md) Weitere Informationen finden Sie unter [Abrufen von Daten vom lokalen Computer.](obtaining-data-from-the-local-computer.md) Die entsprechende C++-Schnittstelle ist [**IWSManSession.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**Wsman**](wsman.md)
</dt> <dd>

Stellt Methoden und Eigenschaften bereit, die verwendet werden, um eine neue Sitzung zu erstellen oder eine eingerichtete Sitzung zu verwalten. Weitere Informationen finden Sie unter [Verwenden Windows Remoteverwaltung.](using-windows-remote-management.md) Die entsprechenden C++-Schnittstellen sind [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) und [**IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows Referenz zur Remoteverwaltung](windows-remote-management-reference.md)
</dt> </dl>

 

 




