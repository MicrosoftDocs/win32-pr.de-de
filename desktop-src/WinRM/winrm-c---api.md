---
title: WinRM C++-API
description: Die Windows Remoteverwaltungsschnittstellen können verwendet werden, um Daten zu erhalten oder Ressourcen auf einem Remotecomputer zu verwalten. Diese API ist in erster Linie für die interne Verwendung vorgesehen. Es wird empfohlen, nach Möglichkeit stattdessen die WinRM-Clientshell-API zu verwenden.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742946"
---
# <a name="winrm-c-api"></a>WinRM C++-API

Die Windows Remoteverwaltungsschnittstellen können verwendet werden, um Daten zu erhalten oder [*Ressourcen auf einem*](windows-remote-management-glossary.md) Remotecomputer zu verwalten. Diese API ist in erster Linie für die interne Verwendung vorgesehen. Es wird empfohlen, nach Möglichkeit [stattdessen die WinRM-Clientshell-API](client-shell-api.md) zu verwenden. Die Schnittstellen entsprechen eng der [WinRM-Skripterstellungs-API.](winrm-scripting-api.md)

Die WinRM-Schnittstellen, die direkt von **IDispatch erben,** verfügen jeweils über ein entsprechendes Skriptobjekt. Weitere Informationen finden Sie in der [WinRM-Skripterstellungs-API.](winrm-scripting-api.md)

Für Multithreadanwendungen unterstützt WinRM keine separaten Threads, die auf dasselbe [**IWSMAN-Objekt**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) zugreifen.

Die folgenden Schnittstellen werden von WinRM bereitgestellt.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Stellt Methoden und Eigenschaften zum Erstellen einer neuen Sitzung und Zum Verwalten einer eingerichteten Sitzung verwendet. [**WSMan ist**](wsman.md) das entsprechende Skriptobjekt.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Stellt Methoden und Eigenschaften zum Erstellen eines neuen [**IWSManResourceLocator-Werts zur**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) Diese Methode ist für das [**WSMan-Skriptobjekt**](wsman.md) verfügbar.

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Definiert den Benutzernamen und das Kennwort, die für Remoteverbindungen verwendet werden. [**ConnectionOptions ist**](connectionoptions.md) das entsprechende Skriptobjekt.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Definiert die netzwerkbetriebs- und -eigenschaften, die für die Sitzung verfügbar sind. [**Session**](session.md) ist das entsprechende Skriptobjekt.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Stellt eine Auflistung von Ergebnissen dar, die beim Aufzählen einer Ressource zurückgegeben werden. [**Enumerator ist**](enumerator.md) das entsprechende Skriptobjekt.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Gibt den Pfad zu einer Ressource an. Sie können ein [**IWSManResourceLocator-Objekt**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in [**Sitzungsobjektvorgängen**](session.md) verwenden. [**ResourceLocator**](resourcelocator.md) ist das entsprechende Skriptobjekt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Remoteverwaltungsreferenz](windows-remote-management-reference.md)
</dt> </dl>

 

 




