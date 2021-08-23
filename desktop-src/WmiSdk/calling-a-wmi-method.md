---
title: Aufrufen einer WMI-Methode
description: Der Hauptzweck von WMI besteht im Bereitstellen des Zugriffs auf Klassen und Instanzen, die Objekte in Ihrem Netzwerk darstellen.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1de14f06388454228528d5a419b551ae2ed0d72c82e3b78c9e04855db6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051048"
---
# <a name="how-to-call-a-wmi-method"></a>Aufrufen einer WMI-Methode

Der Hauptzweck von WMI besteht im Bereitstellen des Zugriffs auf Klassen und Instanzen, die Objekte in Ihrem Netzwerk darstellen. Diese Klassen und Instanzen werden von Anbietern unterstützt. Beispielsweise werden alle Instanzen, die Standardhardwaregeräte in Ihrem Unternehmen darstellen, z. B. [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) oder [**Win32 \_ Printer,**](/windows/desktop/CIMWin32Prov/win32-printer)vom Win32-Anbieter unterstützt. Ebenso können Sie über den Ereignisprotokollanbieter auf das Ereignisprotokoll und über den Registrierungsanbieter auf die Registrierung zugreifen.

Die Methoden, die WMI in Schnittstellen wie [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) oder Skriptobjekten wie [**SWbemServices**](swbemservices.md)implementiert, sind in erster Linie für das generische Abrufen und Bearbeiten von Daten vorgesehen, die von einem beliebigen Anbieter bereitgestellt werden. Verwenden Sie beispielsweise [**SWbemServices.InstancesOf,**](swbemservices-instancesof.md) um alle Instanzen des [**Win32-Prozesses \_**](/windows/desktop/CIMWin32Prov/win32-process) in einer Teilmenge von Unternehmenscomputern zu erhalten. Anschließend können Sie die Win32-Anbietermethode [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) für jedes **Win32 \_ Process-Objekt** aufrufen.

Im folgenden Beispiel wird die [**GetOwnerSid-Methode**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) als Automatisierungsmethode für das Process-Objekt aufgerufen. Eine WMI-Methode, z. B. die für [**SWbemObject definierte**](swbemobject.md) [**\_ Path-Methode,**](swbemobject-path-.md) kann auch für das **Process-Objekt aufgerufen** werden.


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



Der tatsächliche Prozess der Verwendung der WMI-Methoden ist identisch mit der Verwendung Windows COM- oder Automatisierungsschnittstelle. Weitere Informationen finden Sie unter [COM](../cossdk/component-services-portal.md) und [Erstellen einer WMI-Anwendung oder Skript.](creating-a-wmi-application-or-script.md) Weitere Informationen zu den Schnittstellen, die WMI unterstützt, finden Sie unter [COM-API für WMI](com-api-for-wmi.md) und [Skript-API für WMI.](scripting-api-for-wmi.md)

Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
