---
title: WinRM-Skript-API
description: Windows-Remoteverwaltung Skript Objekte werden als Ebene oberhalb des WS-Management Protokolls implementiert.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338210"
---
# <a name="winrm-scripting-api"></a>WinRM-Skript-API

Windows-Remoteverwaltung Skript Objekte werden als Ebene oberhalb der [WS-Management-Protokoll](ws-management-protocol.md)implementiert. Mit den Skript Objekten können Sie Daten abrufen oder [*Ressourcen*](windows-remote-management-glossary.md) auf lokalen Computern und Remote Computern verwalten.

## <a name="ws-management-objects"></a>WS-Management Objekte

Jedes Skript Objekt verfügt über eine entsprechende C++-Schnittstelle. Weitere Informationen finden Sie unter [WinRM C++ API](winrm-c---api.md) und [Scripting in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md).

Die folgenden Objekte werden von der WinRM-Skript-API bereitgestellt.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Definiert den Benutzernamen und das Kennwort, die für Remote Verbindungen verwendet werden. Der Benutzername und das Kennwort werden übergeben, wenn die [**createconnectionoptions**](wsman-createconnectionoptions.md) -Methode aufgerufen wird. Weitere Informationen finden Sie unter Abrufen [von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md). Die entsprechende C++-Schnittstelle ist [**iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)
</dt> <dd>

Stellt eine Auflistung von Ergebnissen dar, die beim Auflisten einer Ressource zurückgegeben werden. Weitere Informationen finden Sie unter [auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md). Die entsprechende C++-Schnittstelle ist [**iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Gibt den Pfad zu einer Ressource an. Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt anstelle eines [*Ressourcen-URIs*](windows-remote-management-glossary.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwenden, z. b. " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)". Die entsprechende C++-Schnittstelle ist [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sitzung**](session.md)
</dt> <dd>

Definiert die Netzwerk Vorgänge und-Eigenschaften, die für die Sitzung verfügbar sind, z. b [**. Session. Get**](session-get.md), [**Session. Enumerate**](session-enumerate.md), [**Session. aufrufen**](session-invoke.md). Weitere Informationen finden Sie unter Abrufen [von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md). Die entsprechende C++-Schnittstelle ist [**iwsmansession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMAN**](wsman.md)
</dt> <dd>

Stellt Methoden und Eigenschaften zur Verfügung, die zum Erstellen einer neuen Sitzung oder zum Verwalten einer eingerichteten Sitzung verwendet werden. Weitere Informationen finden Sie unter [Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md). Die entsprechenden C++-Schnittstellen sind [**iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) und [**iwsmanex**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 




