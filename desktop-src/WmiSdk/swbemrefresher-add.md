---
description: Die Methode "taubemaktualisierer. Add" fügt der Auflistung im "Swap-Aktualisierer"-Objekt ein neues ""-Objekt "-Objekt" aus. Das taubemfreshableitem-Objekt wird in die Auflistung im Objekt "Swap-Aktualisierungs Programm" versetzt.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Taubemaktusher. Add-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351199"
---
# <a name="swbemrefresheradd-method"></a>Methode ' Swap. Add '

Die Methode " **taubemaktualisierer. Add** " fügt der Auflistung im " [**Swap**](swbemrefresher.md) -Aktualisierer" [**-Objekt ein neues "**](swbemrefreshableitem.md) "-Objekt "-Objekt" aus.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
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

*"straumpcepath"* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den relativen Pfad des-Objekts im-Namespace enthält. Der Pfad muss eine-Instanz enthalten. Die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft des zurückgegebenen " [**taubemfreshableitem**](swbemrefreshableitem.md) "-Objekts stellt den Index des-Objekts in der Aktualisierungs-Auflistung dar.

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

Wenn der Aufruf erfolgreich ist, wird ein Objekt vom Typ " [**taubemerfrischendes ableitem**](swbemrefreshableitem.md) " zurückgegeben, das ein einzelnes Aktualisier bares Objekt enthält.

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

 

 




