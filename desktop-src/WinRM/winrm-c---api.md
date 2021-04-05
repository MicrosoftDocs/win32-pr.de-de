---
title: WinRM-C++-API
description: Die Windows-Remoteverwaltung Schnittstellen können zum Abrufen von Daten oder zum Verwalten von Ressourcen auf einem Remote Computer verwendet werden. Diese API ist in erster Linie für die interne Verwendung vorgesehen. Es wird empfohlen, die WinRM-ClientShell-API zu verwenden, wenn möglich.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947874"
---
# <a name="winrm-c-api"></a>WinRM-C++-API

Die Windows-Remoteverwaltung Schnittstellen können zum Abrufen von Daten oder zum Verwalten von [*Ressourcen*](windows-remote-management-glossary.md) auf einem Remote Computer verwendet werden. Diese API ist in erster Linie für die interne Verwendung vorgesehen. Es wird empfohlen, die [WinRM-ClientShell-API](client-shell-api.md) zu verwenden, wenn möglich. Die Schnittstellen entsprechen eng der [WinRM-Skript-API](winrm-scripting-api.md).

Die WinRM-Schnittstellen, die direkt von **IDispatch** erben, verfügen jeweils über ein entsprechendes Skript Objekt. Weitere Informationen finden Sie in der [WinRM-Skript-API](winrm-scripting-api.md).

Bei Multithreadanwendungen unterstützt WinRM keine separaten Threads, die auf dasselbe [**iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) -Objekt zugreifen.

Die folgenden Schnittstellen werden von WinRM bereitgestellt.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**Iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Stellt Methoden und Eigenschaften bereit, mit denen eine neue Sitzung erstellt und eine festgelegte Sitzung verwaltet wird. [**WSMAN**](wsman.md) ist das entsprechende Skript Objekt.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**Iwsmanex**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Stellt Methoden und Eigenschaften zur Verfügung, die zum Erstellen eines neuen [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)verwendet werden. Diese Methode ist für das [**WSMAN**](wsman.md) -Skript Objekt verfügbar.

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**Iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Definiert den Benutzernamen und das Kennwort, die für Remote Verbindungen verwendet werden. [**ConnectionOptions**](connectionoptions.md) ist das entsprechende Skript Objekt.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Definiert die Netzwerk Vorgänge und-Eigenschaften, die für die Sitzung verfügbar sind. Die [**Sitzung**](session.md) ist das entsprechende Skript Objekt.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**Iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Stellt eine Auflistung von Ergebnissen dar, die beim Auflisten einer Ressource zurückgegeben werden. [**Enumerator**](enumerator.md) ist das entsprechende Skript Objekt.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**Iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Gibt den Pfad zu einer Ressource an. Sie können ein [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) -Objekt anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwenden. [**ResourceLocator**](resourcelocator.md) ist das entsprechende Skript Objekt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 




