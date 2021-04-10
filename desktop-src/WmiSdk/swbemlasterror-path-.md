---
description: Die Path- \_ Eigenschaft des "errbemlasterror"-Objekts gibt ein "errbeapbjectpath"-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042474"
---
# <a name="swbemlasterrorpath_-property"></a>' Swap. Path '- \_ Eigenschaft

Die **path \_** -Eigenschaft des " [**errbemlasterror**](swbemlasterror.md) "-Objekts gibt ein " [**errbeapbjectpath**](swbemobjectpath.md) "-Objekt zurück, das den Objekt Pfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objekt Pfad erfordern.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Nur die [**Class**](swbemobjectpath-class.md) -Eigenschaft der zurückgegebenen [**errbemubjectpath**](swbemobjectpath.md) -Instanz kann geändert werden. Wenn Sie versuchen, eine andere Eigenschaft zu ändern, oder wenn Sie versuchen [**, die Methoden**](swbemobjectpath-setasclass.md) " [**-Methode"**](swbemobjectpath-setassingleton.md) oder "-Methode" aufzurufen, wird die Fehlermeldung " **wbemErrReadOnly**" angezeigt.

Aus diesem Grund können Sie das Objekt " [**errbemnamedvalueset**](swbemnamedvalueset.md) ", das den Wert der [**Keys**](swbemobjectpath-keys.md) -Eigenschaft der zurückgegebenen " [**errbemubjectpath**](swbemobjectpath.md) "-Instanz ist, nicht ändern. Wenn Sie versuchen, die [**Add**](swbemnamedvalueset-add.md)-, [**Remove**](swbemnamedvalueset-remove.md)-oder [**DeleteAll**](swbemnamedvalueset-deleteall.md) -Methoden für diesen Wert aufzurufen, erhalten Sie einen **wbemErrReadOnly** -Fehler. Außerdem ist es nicht möglich, einen aus dieser Sammlung erhaltenen " [**Swap Name**](swbemnamedvalue.md) "-Wert zu ändern. Wenn Sie versuchen, die [**value**](swbemnamedvalue-value.md) -Eigenschaft zu ändern, wird derselbe Fehlercode zurückgegeben.

Wenn Sie jedoch " [**errbemubject. \_ Clone**](swbemobject-clone-.md) " zum Erstellen einer Kopie aufruft, ist die [**path \_**](swbemobject-path-.md) -Eigenschaft der Kopie vollständig änderbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Fehler<br/>                                                        |
| IID<br/>                      | IID \_ iswbemlasterror<br/>                                                         |



 

 




