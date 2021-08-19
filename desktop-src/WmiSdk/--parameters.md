---
description: Definiert die Eingabe- und Ausgabeparameter für Methoden.
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
ms.openlocfilehash: a2f39cb7b88977c8f61e562badaa6cbda7a5004fc2d0edf70eb59c6276070efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110565"
---
# <a name="__parameters-class"></a>\_\_PARAMETERS-Klasse

Die **\_ \_ PARAMETERS-Systemklasse** ist eine abstrakte Klasse, die die Eingabe- und Ausgabeparameter für Methoden definiert. Sie wird auch verwendet, um Eingabe- und Ausgabeparameterwerte zwischen einem WMI-Client und einem Methodenanbieter zu übergeben.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Member

Die **\_ \_ PARAMETERS-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um eine Methode in einer Benutzerklasse zu definieren, erstellt ein WMI-Client eine Kopie der **\_ \_ PARAMETERS-Klasse** und fügt eine Eigenschaft für jeden Eingabeparameter in einer Methode hinzu. Wenn die Methode einen Rückgabewert oder Ausgabeparameter enthält, muss eine weitere Kopie von **\_ \_ PARAMETERS** erstellt werden. Wenn die Methode einen Rückgabewert zurückgibt, muss der Client eine Eigenschaft namens **ReturnValue** hinzufügen. Der Methodenanbieter speichert dann die Methodenparameter mit einem Aufruf von [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Um eine Methode aufzurufen, ruft ein Client Folgendes nacheinander auf:

1.  [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) zum Abrufen einer Kopie der **\_ \_ PARAMETERS-Klasse,** die von [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)gespeichert wird.
2.  [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), und legt dann eine Eigenschaft für jeden Eingabeparameter auf die -Methode fest.
3.  [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) oder [**IWbemServices::ExecMethodAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) um die Methode auszuführen.

Nachdem die Ausführung der Methode abgeschlossen ist, kann eine andere **\_ \_ PARAMETERS-Klasseninstanz** zurückgegeben werden, wenn die Methode über Ausgabeparameter oder einen Rückgabewert verfügt.

-   Wenn die Methode mithilfe von [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)aufgerufen wurde, wird die **\_ \_ PARAMETERS-Instanz** als Ausgabeargument zurückgegeben.
-   Wenn die Methode mit [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)aufgerufen wurde, wird die **\_ \_ PARAMETERS-Instanz** als Parameter an [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 




