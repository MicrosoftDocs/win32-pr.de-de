---
description: Die Path- \_ Eigenschaft des "errbemubject"-Objekts gibt ein "errbemubjectpath"-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: SWbemObject.Path_-Eigenschaft (wbemdisp. h)
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
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216702"
---
# <a name="swbemobjectpath_-property"></a>"Errbemubject. Path"- \_ Eigenschaft

Die **path \_** -Eigenschaft des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbemubjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Nur die [**Class**](swbemobjectpath-class.md) -Eigenschaft der zurückgegebenen [**errbemubjectpath**](swbemobjectpath.md) -Instanz kann geändert werden. Wenn Sie versuchen, eine andere Eigenschaft zu ändern, oder wenn Sie versuchen, die Methoden " [**stasclass**](swbemobjectpath-setasclass.md) " oder " [**sstassingleton**](swbemobjectpath-setassingleton.md)" aufzurufen, wird ein **wbemErrReadOnly** -Fehler ausgegeben.

Aus diesem Grund können Sie das Objekt " [**errbemnamedvalueset**](swbemnamedvalueset.md) ", das den Wert der [**Keys**](swbemobjectpath-keys.md) -Eigenschaft der zurückgegebenen " [**errbemubjectpath**](swbemobjectpath.md) "-Instanz ist, nicht ändern. Wenn Sie versuchen, die [**Add**](swbemnamedvalueset-add.md)-, [**Remove**](swbemnamedvalueset-remove.md)-oder [**DeleteAll**](swbemnamedvalueset-deleteall.md) -Methoden für diesen Wert aufzurufen, erhalten Sie einen wbemErrReadOnly-Fehler. Außerdem ist es nicht möglich, einen aus dieser Sammlung erhaltenen " [**Swap Name**](swbemnamedvalue.md) "-Wert zu ändern. Wenn Sie versuchen, die **value** -Eigenschaft zu ändern, wird derselbe Fehlercode zurückgegeben.

Wenn Sie jedoch " [**errbemubject. Clone \_**](swbemobject-clone-.md) " aufrufen, um eine Kopie zu erstellen, ist die Eigenschaft " [**errbemubjectpath. Path**](swbemobjectpath-path.md) " der Kopie vollständig änderbar.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel, das aus [Auflisten aller WMI-cimV2-Klassen](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in der TechNet-Galerie stammt, wird die Path-Eigenschaft verwendet, \_ um alle WMI cimV2-Klassen aufzulisten.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



 

 




