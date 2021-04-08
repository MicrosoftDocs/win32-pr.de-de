---
description: Fügt dem Objekt "Swap-Aktualisierungs Programm" einen neuen Enumerator hinzu. Dieser Enumerator gilt für alle Instanzen der-Klasse, die im Parameter "-Parameter" angegeben sind.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Slibemaktusher. AddEnum-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761400"
---
# <a name="swbemrefresheraddenum-method"></a>Methode ' slibemfreshsher. AddEnum '

Die Methode " **Swap. AddEnum** " fügt dem Objekt "slibemaktusher" [](swbemrefresher.md) einen neuen Enumerator hinzu. Dieser Enumerator gilt für alle Instanzen der-Klasse *, die im Parameter "* -Parameter" angegeben sind.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemservice* 
</dt> <dd>

Erforderlich. Ein-Objekt, [**das eine Verbindung**](swbemservices.md) mit dem Namespace darstellt, in dem sich das dem Aktualisierungs Programm hinzugefügte Objekt befindet.

</dd> <dt>

*Klasse* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die die Klasse enthält, die dem Aktualisierungs Programm hinzugefügt wird. Diese Klasse wird als Enumerator der Instanzen der-Klasse verwendet. Die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft des zurückgegebenen " [**taubemfreshableitem**](swbemrefreshableitem.md) "-Elements stellt den Index des Enumerators in der Aktualisierungs-Auflistung dar.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine Zeichenfolge, die den Objekt Pfad des Objekts enthält, für das die Methode ausgeführt wird.

</dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der- [**Befehl**](swbemrefreshableitem.md) erfolgreich ausgeführt wurde, wird ein-Objekt mit einem-Enumerator zurückgegeben, das einen Enumerator für alle Instanzen der angegebenen Klasse enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschprogramm<br/>                                                        |
| IID<br/>                      | IID \_ iswbemfreshsher<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Aktualisierungs Programm**](swbemrefresher.md)
</dt> </dl>

 

 




