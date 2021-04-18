---
description: Das Löschen einer Instanz ist der häufigste DELETE-Befehl, den Sie in WMI wahrscheinlich ausführen.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Löschen einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345273"
---
# <a name="deleting-an-instance"></a>Löschen einer Instanz

Das Löschen einer Instanz ist der häufigste DELETE-Befehl, den Sie in WMI wahrscheinlich ausführen. Wie beim Löschen einer Klasse ist der tatsächliche Befehl recht einfach. WMI unterscheidet sich jedoch je nach dem zu löschenden Instanztyp ganz anders. Wenn die Instanz statisch ist, löscht WMI einfach die Instanz aus dem WMI-Repository. Weitere Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**pragma deleteclass**](pragma-deleteclass.md) -Präprozessorbefehl.

Wenn die Instanz dynamisch ist, muss WMI auf den Anbietern, die für die folgenden Klassen zuständig sind, [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) aufrufen:

-   Die Klasse, die Besitzer der-Instanz ist.
-   Jede übergeordnete Klasse der Klasse, die die Instanz besitzt.
-   Jede Unterklasse der-Klasse, die Besitzer der-Instanz ist.

Der Erfolg der Löschung hängt von der obersten nicht abstrakten Klasse der ursprünglichen Instanz ab. Wenn der Anbieter für eine oberste, nicht abstrakte Klasse den Löschvorgang abgeschlossen hat, ist der Vorgang erfolgreich. Weitere Informationen finden Sie im Abschnitt "Hinweise" unter [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).

Die [com-API für WMI](com-api-for-wmi.md) verfügt über verschiedene Methoden zum Löschen einer Instanz und zum Löschen eines Objekts.

Im folgenden Verfahren wird beschrieben, wie C++ verwendet wird, um eine Instanz einer Basisklasse oder abgeleiteten Klasse zu löschen.

**So löschen Sie eine Instanz einer Basisklasse oder abgeleiteten Klasse mithilfe von C++**

-   Entweder die [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) -oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) -Methode aufrufen.

    Wie der Name vermuten lässt, löscht " [**Delta einstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) " eine Instanz asynchron, während " [**Delta einstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) " eine Instanz synchron löscht. Um **Delta einstanceasync** verwenden zu können, müssen Sie auch ein [**IWbemObjectSink**](iwbemobjectsink.md) -Objekt implementieren.

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

Die [Skript-API für WMI](scripting-api-for-wmi.md) verwendet dieselben Methoden, um entweder ein Klassenobjekt oder eine Instanz zu löschen.

Im folgenden Verfahren wird die Verwendung von VBScript zum Löschen einer Instanz einer Basisklasse oder abgeleiteten Klasse beschrieben.

**So löschen Sie eine Instanz einer Basisklasse oder abgeleiteten Klasse mithilfe von VBScript**

-   Aufrufen der Methoden " [**errbemjebject \_ . Delete**](swbemobject-delete-.md) " oder " [**errbemubject. \_ deleteasync**](swbemobject-deleteasync-.md) ".

    Wie der Name vermuten lässt, löscht [**Delete \_**](swbemobject-delete-.md) eine Instanz synchron, während [**deleteasync \_**](swbemobject-deleteasync-.md) eine Instanz asynchron löscht. Weitere Informationen zum asynchronen Löschen einer Instanz finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

    Im folgenden Beispiel wird beschrieben, wie eine Instanz mit VBScript gelöscht wird.

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

 

 



