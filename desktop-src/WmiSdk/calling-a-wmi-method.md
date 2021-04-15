---
title: Vorgehensweise beim aufzurufen einer WMI-Methode
description: Der Hauptzweck von WMI besteht darin, den Zugriff auf Klassen und Instanzen bereitzustellen, die Objekte in Ihrem Netzwerk darstellen.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529555"
---
# <a name="how-to-call-a-wmi-method"></a>Vorgehensweise beim aufzurufen einer WMI-Methode

Der Hauptzweck von WMI besteht darin, den Zugriff auf Klassen und Instanzen bereitzustellen, die Objekte in Ihrem Netzwerk darstellen. Diese Klassen und Instanzen werden von Anbietern unterstützt. Beispielsweise werden alle Instanzen, die Standard Hardware Geräte in Ihrem Unternehmen darstellen, wie z. b. [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) oder [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer), vom Win32-Anbieter unterstützt. Auf ähnliche Weise können Sie über den Ereignisprotokoll Anbieter und die Registrierung über den Registrierungs Anbieter auf das Ereignisprotokoll zugreifen.

Die von WMI implementierten Methoden, wie z. b. [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) oder Skript Objekte wie z. b. " [**Swap Services**](swbemservices.md)", sind hauptsächlich für die generische Erfassung und Bearbeitung von Daten, die von einem Anbieter bereitgestellt Verwenden Sie z. b. " [**Swap Services. InstancesOf**](swbemservices-instancesof.md) ", um alle Instanzen des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) in einer Teilmenge von Unternehmens Computern abzurufen. Sie können dann die Win32-Anbieter Methode " [**GetOwnerSID**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) " für jedes **Win32- \_ Prozess** Objekt aufrufen.

Im folgenden Beispiel wird die [**GetOwnerSID**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) -Methode als Automatisierungs Methode für das Process-Objekt aufgerufen. Eine WMI-Methode, z. b. die für " [**Swap**](swbemobject.md) " definierte [**Pfad \_**](swbemobject-path-.md) Methode, kann auch für das **Prozess** Objekt aufgerufen werden.


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



Der tatsächliche Prozess der Verwendung der WMI-Methoden ist identisch mit der Verwendung anderer Windows com-oder Automatisierungs Schnittstellen. Weitere Informationen finden Sie unter [com](../cossdk/component-services-portal.md) und [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md). Weitere Informationen zu den Schnittstellen, die von WMI unterstützt werden, finden Sie unter [com-API für WMI](com-api-for-wmi.md) und [Skript-API für WMI](scripting-api-for-wmi.md).

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
