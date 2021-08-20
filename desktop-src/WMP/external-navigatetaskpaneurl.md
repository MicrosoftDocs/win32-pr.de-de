---
title: External.NavigateTaskPaneURL-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.NavigateTaskPaneURL-Methode
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- NavigateTaskPaneURL-Methode Windows Media Player
- NavigateTaskPaneURL-Methode Windows Media Player , External-Klasse
- Externe Klasse Windows Media Player , NavigateTaskPaneURL-Methode
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebcf8d799452a9966355f644f00ac5c4aecc4c066374254e8e580431b756b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649030"
---
# <a name="externalnavigatetaskpaneurl-method"></a>External.NavigateTaskPaneURL-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **NavigateTaskPaneURL-Methode** öffnet eine Webseite im angegebenen Aufgabenbereich und ändert den Fokus in den angegebenen Bereich.

## <a name="syntax"></a>Syntax


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKeyName* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Schlüsselnamen für den Onlineshop enthält. (erforderlich)

</dd> <dt>

*bstrTaskPane* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des Aufgabenbereichs enthält, in dem die Webseite geöffnet wird. (erforderlich)

</dd> <dt>

*bstrParams* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die Abfragezeichenfolgenparameter enthält, die an die URL angefügt werden sollen, die vom **Navigate-Element** des ServiceInfo-Dokuments angegeben wird. (Optional)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Navigieren zu einem Bereich, den Ihr Onlineshop nicht unterstützt, kann dazu führen, dass sich der aktuelle Onlineshop ändert.

Der für *bstrParams* angegebene Wert ist nur gültig, wenn **NavigateTaskPaneURL** von Webseiten aufgerufen wird, die vom Onlineshop bereitgestellt werden.

In der folgenden Tabelle sind die gültigen Werte für *bstrTaskPane* und der zugehörige Aufgabenbereich für jeden aufgeführt.



| Wert            | Aufgabenbereich                      |
|------------------|--------------------------------|
| **ServiceTask1** | Erster Aufgabenbereich des Onlineshops.  |
| **ServiceTask2** | Zweiter Aufgabenbereich des Onlineshops. |
| **ServiceTask3** | Der dritte Aufgabenbereich des Onlineshops.  |



 

Ihr Webseitencode sollte beim Laden einen Wert für [External.SelectedTaskPane](external-selectedtaskpane.md) angeben, um sicherzustellen, dass die richtige Aufgabenbereichsschaltfläche nach Abschluss der Navigation hervorgehoben ist.

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie **NavigateTaskPaneURL** die URL der Webseite erstellt, die für **ServiceTask1** angezeigt werden soll.

Beispiel für das **Navigate-Element:**


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Beispielaufruf der **NavigateTaskPaneURL-Methode:**


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Beispiel für die resultierende URL, die für die Webseite verwendet wird, die in **ServiceTask1** angezeigt wird:


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlineshops vom Typ 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





