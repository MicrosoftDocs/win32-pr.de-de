---
description: Definiert die Eingabe-und Ausgabeparameter für Methoden.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358952"
---
# <a name="__parameters-class"></a>\_\_Parameters-Klasse

Die **\_ \_ Parameters** -System Klasse ist eine abstrakte Klasse, die die Eingabe-und Ausgabeparameter für Methoden definiert. Außerdem werden Sie verwendet, um Eingabe-und Ausgabeparameter Werte zwischen einem WMI-Client und einem Methoden Anbieter zu übergeben.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Member

Die **\_ \_ Parameters** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Zum Definieren einer Methode in einer Benutzerklasse erstellt ein WMI-Client eine Kopie der **\_ \_ para** meters-Klasse und fügt eine Eigenschaft für jeden Eingabeparameter in einer Methode hinzu. Wenn die Methode einen Rückgabewert oder Ausgabeparameter enthält, muss eine andere Kopie der **\_ \_ Parameter** erstellt werden. Wenn die Methode einen Rückgabewert zurückgibt, muss der Client eine Eigenschaft mit dem Namen " **ReturnValue**" hinzufügen. Der Methoden Anbieter speichert dann die Methoden Parameter mit einem-Befehl, der [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)aufruft.

Um eine Methode aufzurufen, Ruft ein Client die folgenden Reihenfolge auf:

1.  [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) zum Abrufen einer Kopie der **\_ \_ Parameters** -Klasse, die von [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)gespeichert wird.
2.  [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), und legt dann eine Eigenschaft für jeden Eingabeparameter für die Methode fest.
3.  [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) zum Ausführen der Methode.

Nachdem die Ausführung der Methode abgeschlossen ist, kann eine andere **\_ \_ Parameter** Klasseninstanz zurückgegeben werden, wenn die Methode über Ausgabeparameter oder einen Rückgabewert verfügt.

-   Wenn die Methode mithilfe von [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)aufgerufen wurde, wird die **\_ \_ Parameter** Instanz als Ausgabe Argument zurückgegeben.
-   Wenn die Methode mithilfe von [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)aufgerufen wurde, wird die **\_ \_ Parameter** Instanz als Parameter an [**iwbemubjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)Expression zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 




