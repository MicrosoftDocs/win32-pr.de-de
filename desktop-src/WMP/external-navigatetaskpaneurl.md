---
title: Extern. navigatetaskpaneurl-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. navigatetaskpaneurl-Methode
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Navigatetaskpaneurl-Methode, Windows Media Player
- Navigatetaskpaneurl-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, navigatetaskpaneurl-Methode
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
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371978"
---
# <a name="externalnavigatetaskpaneurl-method"></a>Extern. navigatetaskpaneurl-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **navigatetaskpaneurl** -Methode öffnet eine Webseite im angegebenen Aufgabenbereich und ändert den Fokus auf den angegebenen Bereich.

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

*btrekeyname* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Schlüsselnamen für den Online Store enthält. (erforderlich)

</dd> <dt>

*bstrautaskpane* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Aufgabenbereichs enthält, in dem die Webseite geöffnet wird. (erforderlich)

</dd> <dt>

*bstrinbiams* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die die Abfrage Zeichenfolgen-Parameter enthält, die an die URL angefügt werden sollen, die vom **Navigate** -Element des servicinput (Optional)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie zu einem Bereich navigieren, den der Online Shop nicht unterstützt, kann sich der aktuelle Online Shop ändern.

Der für *bstrinparameams* angegebene Wert ist nur gültig, wenn **navigatetaskpaneurl** von Webseiten aufgerufen wird, die vom Online Store bereitgestellt werden.

In der folgenden Tabelle sind gültige Werte für *bstrautaskpane* und der zugehörige Aufgabenbereich für jeden aufgeführt.



| Wert            | Aufgabenbereich                      |
|------------------|--------------------------------|
| **ServiceTask1** | Der erste Aufgabenbereich für den Online Shop.  |
| **ServiceTask2** | Zweiter Online Store-Aufgabenbereich. |
| **ServiceTask3** | Dritter Aufgabenbereich für den Online Shop.  |



 

Der Webseiten Code sollte beim Laden einen Wert für " [extern. selectedtaskpane](external-selectedtaskpane.md) " angeben, um sicherzustellen, dass die richtige Aufgabenbereichs Schaltfläche nach Abschluss der Navigation hervorgehoben wird.

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie **navigatetaskpaneurl** die URL der Webseite erstellt, die für **ServiceTask1** angezeigt werden soll.

Beispiel für das **Navigate** -Element:


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Beispiel für einen aufzurufenden Befehl der **navigatetaskpaneurl** -Methode:


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Beispiel für eine resultierende URL, die für die in **ServiceTask1** angezeigte Webseite verwendet wird:


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

[**Externes Objekt für den Typ 2-Online Speicher**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Extern. selectedtaskpane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





