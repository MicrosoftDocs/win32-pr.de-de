---
description: Anbieter, es sei denn, Sie sind entkoppelte Anbieter, die in einer Anwendung ausgeführt werden, werden in einen Wmiprvse.exe Prozess geladen, nicht durch Svchost.exe mit einem Winmgmt.exe Prozess. Weitere Informationen finden Sie unter Anbieter Hosting und-Sicherheit.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Debuganbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959378"
---
# <a name="debugging-providers"></a>Debuganbieter

Anbieter, es sei denn, Sie sind [*entkoppelte Anbieter*](gloss-d.md) , die in einer Anwendung ausgeführt werden, werden in einen Wmiprvse.exe Prozess geladen, nicht durch Svchost.exe mit einem Winmgmt.exe Prozess. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

Beim Anhalten an einem Haltepunkt friert der Visual Studio-Debugger den gesamten Anbieter Host Prozess, der in der Regel der freigegebene Host Wmiprvse.exe ist. Dies verhindert den Betrieb anderer in diesem Prozess gehosteter Komponenten, einschließlich der WMI-Server-Explorer Erweiterung. Client Anwendungen, die den Anbieter aufzurufen, werden ebenfalls blockiert. Die Probleme, die sich auf Windows 2000 und früher ergeben, sind schlimmer, da der Anbieter in den WMI-Dienst Prozess (Winmgmt.exe) geladen wird.

Wenn Sie WMI-Server-Explorer in einer anderen-Instanz ausführen, wird die Visual Studio-IDE nicht fixiert, und Sie können den Breakpoint freigeben. Es wird empfohlen, dass Sie den Anbieter während der Entwicklungsphase in einem separaten Hostingprozess ausführen, sodass der Prozess, der an einem Haltepunkt angehalten wird, nur den Prozess, der den Anbieter gehostet, abstürzt. Die anderen Funktionen in WMI sind auch für WMI-Server-Explorer und alle anderen WMI-basierten Anwendungen oder Skripts zugänglich. Wenn der Anbieter abstürzt, wirkt sich dies auch nicht auf den Betrieb anderer Anbieter aus, die in denselben Host Prozess geladen werden.

Damit der Anbieter in einem eigenen Host Prozess geladen wird, ändern Sie die Anbieter Registrierung so, dass die [**\_ \_ Win32Provider. hostingmodel**](--win32provider.md) -Eigenschaft auf festgelegt `NetworkServiceHost:[MyProvider]` wird, wobei MyProvider eine beliebige Zeichenfolge sein kann, die Ihren Anbieter eindeutig identifiziert. Verwenden Sie z. b. den Wert **\_ \_ Win32Provider. CLSID** . Wenn Ihr Anbieter bereit für das Versenden ist, geben Sie **\_ \_ Win32Provider. hostingmodel** an den beabsichtigten Wert zurück, z. b. **networkservicehost**.

Wenn Sie das Laden von Anbietern nicht debuggen, können Sie die [**Load-Methode der \_ Klasse der MSFT-Anbieter**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) aufzurufen, um das Laden des Anbieters zu erzwingen, dann an den Wmiprvse.exe Prozess anzufügen, der die dll geladen hat, und nach Bedarf Debuggen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Problembehandlung](wmi-troubleshooting.md)
</dt> <dt>

[WMI-Fehler Behebungs Klassen](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
