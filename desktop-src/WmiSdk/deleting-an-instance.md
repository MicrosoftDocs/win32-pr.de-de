---
description: Das Löschen einer Instanz ist der gängigste Löschbefehl, den Sie wahrscheinlich in WMI ausführen werden.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Löschen einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d5802ef3aceede444f5c3f58983bcbe770406260e7df5a06360144ddea167b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925118"
---
# <a name="deleting-an-instance"></a>Löschen einer Instanz

Das Löschen einer Instanz ist der gängigste Löschbefehl, den Sie wahrscheinlich in WMI ausführen werden. Wie beim Löschen einer Klasse ist der eigentliche Befehl recht einfach. WMI führt jedoch je nach Typ der zu löschenden Instanz eine andere Leistung aus. Wenn die Instanz statisch ist, löscht WMI die Instanz einfach aus dem WMI-Repository. Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**Pragma deleteclass-Präprozessorbefehl.**](pragma-deleteclass.md)

Wenn die Instanz dynamisch ist, muss WMI [**IWbemServices::D eleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) für die Anbieter aufrufen, die für die folgenden Klassen verantwortlich sind:

-   Die Klasse, die die Instanz besitzt.
-   Jede übergeordnete Klasse der Klasse, die die Instanz besitzt.
-   Jede Unterklasse der Klasse, die die Instanz besitzt.

Der Erfolg des Löschvorgangs hängt von der obersten nonabstract-Klasse für die ursprüngliche Instanz ab. Wenn der Anbieter für eine der obersten Nichtabstraktionsklassen den Löschvorgang erfolgreich abschließt, ist der Vorgang erfolgreich. Weitere Informationen finden Sie im Abschnitt "Hinweise" von [**IWbemServices::D eleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).

Die [COM-API für WMI](com-api-for-wmi.md) verfügt über verschiedene Methoden zum Löschen einer Instanz und zum Löschen eines Objekts.

Im folgenden Verfahren wird beschrieben, wie C++ verwendet wird, um eine Instanz einer Basisklasse oder abgeleiteten Klasse zu löschen.

**So löschen Sie eine Instanz einer Basisklasse oder abgeleiteten Klasse mit C++**

-   Rufen Sie entweder die [**Methoden IWbemServices::D eleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) oder [**IWbemServices::D eleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) auf.

    Wie der Name schon sagt, löscht [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) eine Instanz asynchron, während [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) eine Instanz synchron löscht. Um **DeleteInstanceAsync** zu verwenden, müssen Sie auch ein [**IWbemObjectSink-Objekt**](iwbemobjectsink.md) implementieren.

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der gleichen Authentifizierungsebene zurückgegeben wird, die der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchron zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

Die [Skripterstellungs-API für WMI](scripting-api-for-wmi.md) verwendet die gleichen Methoden, um entweder ein Klassenobjekt oder eine Instanz zu löschen.

Das folgende Verfahren beschreibt die Verwendung von VBScript zum Löschen einer Instanz einer Basisklasse oder abgeleiteten Klasse.

**So löschen Sie eine Instanz einer Basisklasse oder abgeleiteten Klasse mit VBScript**

-   Rufen Sie entweder die [**Methoden \_ SWbemObject.Delete**](swbemobject-delete-.md) oder [**SWbemObject.DeleteAsync \_**](swbemobject-deleteasync-.md) auf.

    Wie der Name schon sagt, löscht [**\_ Delete**](swbemobject-delete-.md) eine Instanz synchron, während [**DeleteAsync \_**](swbemobject-deleteasync-.md) eine Instanz asynchron löscht. Weitere Informationen zum asynchronen Löschen einer -Instanz finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

    Im folgenden Beispiel wird beschrieben, wie eine -Instanz mit VBScript gelöscht wird.

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf der gleichen Authentifizierungsebene zurückgegeben wird, die der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchron zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

 

 



