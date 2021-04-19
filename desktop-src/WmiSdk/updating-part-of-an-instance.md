---
description: Gelegentlich kann es vorkommen, dass Sie nur einen Teil einer Instanz aktualisieren möchten.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Aktualisieren eines Teils einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372949"
---
# <a name="updating-part-of-an-instance"></a>Aktualisieren eines Teils einer Instanz

Gelegentlich kann es vorkommen, dass Sie nur einen Teil einer Instanz aktualisieren möchten. Einige Instanzen verfügen z. b. über eine große Anzahl von Eigenschaften. Wenn Sie eine große Anzahl dieser Instanzen aktualisieren müssen, können Sie die Systemleistung beeinträchtigen. Aus diesem Grund können Sie auswählen, dass nur ein Teil der-Instanz aktualisiert wird, und so die Menge an Informationen reduzieren, die Sie an und von WMI senden und abrufen müssen. Allerdings unterstützt WMI nicht direkt Vorgänge für partielle Instanzen oder die meisten Anbieter. Wenn Sie also eine Anwendung schreiben, die partielle instanzvorgänge verwendet, sollten Sie darauf vorbereitet sein, dass Ihre Aufrufe fehlschlagen, wenn der **WBEM \_ e- \_ Anbieter \_ nicht \_** unterstützt oder der Fehlercode **WBEM \_ e \_ nicht \_ unterstützt** in C++ ist. In Skriptsprachen sind die Fehlercodes entweder **wbemErrProviderNotCapable** oder **wbemErrNotSupported**.

Bei der Skripterstellung ist dieser Vorgang nur erforderlich, um die Leistung beim Aktualisieren von einer oder zwei beschreibbaren Eigenschaften in einer sehr großen Anzahl von Objekten über ein Unternehmen zu unterstützen. Andernfalls aktualisieren die normalen VBScript-Aufrufe von " [**errbewbject \_ . Put**](swbemobject-put-.md) " oder " [**errbejebject \_ . putasync**](swbemobject-putasync-.md)", während Sie das gesamte Objekt schreiben, tatsächlich nur die Eigenschaften aktualisieren, für die der Anbieter Schreibzugriff hat.

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von PowerShell ein partielles instanzupdate anfordern.

**So fordern Sie eine teilinstanzaktualisierung mithilfe von PowerShell an**

1.  Rufen Sie den Pfad des Objekts ab, das Sie aktualisieren möchten.

    Sie können den Pfad entweder manuell beschreiben oder das Objekt Abfragen und dann die **\_ \_ path** -Eigenschaft abrufen.

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  Richten Sie eine Hash Tabelle ein, die die Namen der zu aktualisierenden Eigenschaften auflistet, und verwenden Sie diese Hash Tabelle in einem-Befehl von [Set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von c# eine partielle Instanzaktualisierung anfordern.

> [!Note]  
> **System. Management** war der ursprüngliche .NET-Namespace, der für den Zugriff auf WMI verwendet wurde. die APIs in diesem Namespace sind jedoch in der Regel langsamer und werden relativ zu ihren moderneren **Microsoft. Management. Infrastructure** -Entsprechungen nicht auch skaliert.

 

**So fordern Sie eine teilinstanzaktualisierung mithilfe von C an #**

1.  Erstellen Sie ein neues [Management Object](/dotnet/api/system.management.managementobject) -Objekt, das die zu Aktualisier gende Instanz darstellt.

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  Legen Sie den Eigenschafts Wert mit einem Aufrufen von [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_)fest.

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie mit VBScript eine partielle Instanzaktualisierung anfordern.

**So fordern Sie eine teilinstanzaktualisierung mithilfe von VBScript an**

1.  Erstellen Sie ein [**Swap**](swbemnamedvalueset.md) -Kontext Objekt.

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  Fügen Sie die Put-Erweiterungs Werte " \_ \_ Put \_ Extensions" und " \_ \_ Put \_ Ext \_ Client \_ Request" dem Kontext Objekt mithilfe der Methode " [**Swap Name. Add**](swbemnamedvalueset-add.md) " hinzu.

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  Richten Sie ein Array ein, das die Namen der zu aktualisierenden Eigenschaften auflistet, [](swbemnamedvalueset.md) und fügen Sie das Array mit dem Wert der Put-Erweiterung " \_ \_ Put \_ Ext \_ Properties" dem Kontext Objekt "Swap Name" hinzu.

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  Legen Sie den *IFlags* -Parameter des Austauschs "WS- [**imbject. Put \_**](swbemobject-put-.md) " auf " **wbemchangeflagupdateonly**" fest. Ohne dieses Flag schlägt der-Befehl mit einem ungültigen Kontext fehl.

5.  Übergeben Sie Ihr Flag und das Kontext Objekt an den Anbieter in den *objwbemnamedvalueset* -Parametern von " [**errbefubject. Put \_**](swbemobject-put-.md) " oder " [**Swap. putasync \_**](swbemobject-putasync-.md)".

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

Im folgenden Verfahren wird beschrieben, wie Sie eine teilinstanzaktualisierung mithilfe von C++ anfordern.

**So fordern Sie eine teilinstanzaktualisierung mithilfe von C++ an**

1.  Erstellen Sie ein [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Ein Kontext Objekt ist ein Objekt, das WMI verwendet, um weitere Informationen an einen WMI-Anbieter zu übergeben. In diesem Fall verwenden Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt, um den Anbieter anzuweisen, partielle instanzaktualisierungen zu akzeptieren.

2.  Fügen Sie die \_ \_ \_ benannten Werte "Put Extensions" und " \_ \_ Put \_ Ext \_ Client \_ Request" zum [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt hinzu, indem Sie " [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)" aufrufen.

    In der folgenden Tabelle sind die Bedeutung von " \_ \_ Put \_ Extensions" und " \_ \_ Put \_ Ext \_ Client \_ Request" aufgeführt.

    

    | Benannter Wert                     | BESCHREIBUNG                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ Put \_ Extensions"           | **VT \_ Bool** auf **Variant \_ true** festgelegt. Ein-Wert, der angibt, dass ein oder mehrere der anderen Kontext Werte angegeben wurden. Dies ermöglicht eine schnelle Überprüfung des Kontext Objekts innerhalb des Anbieters, um zu bestimmen, ob Updates für Teil Instanzen verwendet werden. |
    | " \_ \_ \_ Ext- \_ Client \_ Anforderung ablegen" | **VT \_ Bool** auf **Variant \_ true** festgelegt. Wird vom Client während der anfänglichen Anforderung festgelegt. Dieser Wert wird verwendet, um Fehler beim erneuten eintreten zu vermeiden.                                                                                                                   |

    

     

3.  Fügen Sie die " \_ \_ Put \_ ext Strict NULLS"-Eigenschaft, "Put ext"-Eigenschaften oder "Set Ext \_ \_ \_ \_ \_ Atomic" \_ \_ \_ \_ \_ in beliebiger Kombination für das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt mit einem weiteren [**callbemcontext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)-Befehl hinzu.

    In der folgenden Tabelle wird die Bedeutung der benannten Werte aufgelistet.

    

    | Benannter Wert                   | BESCHREIBUNG                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ Put \_ Ext \_ Strict \_ NULLS" | **VT \_ Bool** auf **Variant \_ true** festgelegt. Gibt an, dass der Client die Eigenschaften absichtlich auf **VT \_ null** festgelegt hat und erwartet, dass der Schreibvorgang erfolgreich ist. Wenn der Anbieter die Werte nicht auf **null** festlegen kann, sollte ein Fehler gemeldet werden. |
    | " \_ \_ Put \_ Ext- \_ Eigenschaften"    | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) von Zeichen folgen, die eine Liste der zu aktualisierenden Eigenschaften Namen enthalten. Kann allein oder in Kombination mit " \_ \_ Put \_ Ext \_ Properties" verwendet werden. Die Werte befinden sich in der-Instanz, die geschrieben wird.                           |
    | " \_ \_ Put \_ Ext \_ Atomic"        | **VT \_ Bool** auf **Variant \_ true** festgelegt. Gibt an, dass alle Updates gleichzeitig ausgeführt werden müssen (atomarische Semantik), oder der Anbieter muss rückgängig gemacht werden. Es kann kein Teilerfolg geben. Kann allein oder in Kombination mit anderen Flags verwendet werden.     |

    

     

4.  Legen Sie den *IFlags* -Parameter auf das **WBEM- \_ Flag \_ \_ nur aktualisieren** fest. Ohne dieses Flag schlägt der-Befehl mit einem ungültigen Kontext fehl.
5.  Übergeben Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Kontext Objekt in beliebige Aufrufe [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) im *pctX* -Parameter.

    Wenn Sie das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt übergeben, weist der Anbieter an, partielle instanzaktualisierungen zuzulassen. Bei einem vollständigen instanzupdate legen Sie *pctX* auf **null** fest.

    Der Anbieter kann alle notwendigen Eigenschaften schreiben, wenn das im-Befehl vorhandene Kontext Objekt keine " \_ \_ Put \_ Extensions" enthält. Wenn " \_ \_ Put \_ Extensions" im Context-Objekt vorhanden ist, erfordert WMI, dass der Anbieter die Semantik des Vorgangs genau befolgt oder der-Befehl andernfalls fehlschlägt. Weitere Informationen finden Sie unter [Behandeln von Zugriffen auf Abgelehnte Nachrichten in einem Anbieter](impersonating-a-client.md).

 

 
