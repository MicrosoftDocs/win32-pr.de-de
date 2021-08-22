---
description: Die \_ Path-Eigenschaft des SWbemObject-Objekts gibt ein SWbemObjectPath-Objekt zurück, das den Objektpfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objektpfad erfordern.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: SWbemObject.Path_ -Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b87d2ad73fcaea2be2214a962940f154bb6df2b428f98d4646e0cb935ab2859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991990"
---
# <a name="swbemobjectpath_-property"></a>SWbemObject.Path(Eigenschaft) \_

Die **\_ Path-Eigenschaft** des [**SWbemObject-Objekts**](swbemobject.md) gibt ein [**SWbemObjectPath-Objekt**](swbemobjectpath.md) zurück, das den Objektpfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objektpfad erfordern.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Nur die [**Class-Eigenschaft**](swbemobjectpath-class.md) der zurückgegebenen [**SWbemObjectPath-Instanz**](swbemobjectpath.md) kann geändert werden. Wenn Sie versuchen, eine andere Eigenschaft zu ändern oder die Methoden [**SetAsClass**](swbemobjectpath-setasclass.md) oder [**SetAsSingleton**](swbemobjectpath-setassingleton.md)auf aufruft, erhalten Sie einen **wbemErrReadOnly-Fehler.**

Aus diesem Grund können Sie das [**SWbemNamedValueSet-Objekt**](swbemnamedvalueset.md) nicht ändern, das der Wert der [**Keys-Eigenschaft**](swbemobjectpath-keys.md) der zurückgegebenen [**SWbemObjectPath-Instanz**](swbemobjectpath.md) ist. Wenn Sie versuchen, die [**Methoden Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)oder [**DeleteAll**](swbemnamedvalueset-deleteall.md) für diesen Wert auf aufruft, erhalten Sie einen wbemErrReadOnly-Fehler. Darüber hinaus können Sie [**SWbemNamedValue aus dieser**](swbemnamedvalue.md) Sammlung nicht ändern. Versuche, die **Value-Eigenschaft** zu ändern, geben den gleichen Fehlercode zurück.

Wenn Sie jedoch [**SWbemObject.Clone \_**](swbemobject-clone-.md) aufrufen, um eine Kopie zu erstellen, ist die [**SWbemObjectPath.Path-Eigenschaft**](swbemobjectpath-path.md) der Kopie vollständig änderbar.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel aus List All the WMI cimV2 Classes in the TechNet Gallery (Auflisten aller [WMI-cimV2-Klassen](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) im TechNet-Katalog) wird die Path-Eigenschaft verwendet, um alle \_ WMI-CimV2-Klassen auflisten.


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




