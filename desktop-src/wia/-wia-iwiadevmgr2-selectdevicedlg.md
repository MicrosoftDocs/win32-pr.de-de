---
description: 'IWiaDevMgr2::SelectDeviceDlg-Methode: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: IWiaDevMgr2::SelectDeviceDlg-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 344b13ec05e6f1d06011b3555e5b455202e5848b5000e799540d9f7c3160653b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441235"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>IWiaDevMgr2::SelectDeviceDlg-Methode

Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Bilderfassung auswählen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Gibt das übergeordnete Fenster des Dialogfelds **Gerät** auswählen an.

</dd> <dt>

*lDeviceType* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt an, welcher Typ von WIA 2.0-Gerät verwendet werden soll. Eine [Liste der möglichen Werte](-wia-wia-device-type-specifiers.md) finden Sie unter WIA-Gerätetypspezifizierer.

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt das Verhalten des Dialogfelds an. Der Wert kann einer der folgenden sein.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Verwendet das Standardverhalten.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**


</dt> <dd>

Das Dialogfeld wird angezeigt, obwohl es nur ein passendes Gerät gibt.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ in, out\]
</dt> <dd>

Typ: **BSTR \***

Empfängt bei der Ausgabe eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts enthält. Übergeben Sie bei der Eingabe die Adresse eines Zeigers, wenn diese Informationen benötigt werden, oder **NULL,** wenn sie nicht benötigt werden.

</dd> <dt>

*ppItemRoot* \[ out, retval\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des Stammelements der hierarchischen Struktur, das das ausgewählte WIA 2.0-Gerät darstellt. Wenn kein Gerät gefunden wird, empfängt es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                  | Beschreibung                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Das Gerät wurde erfolgreich ausgewählt. <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | Der Benutzer hat das Dialogfeld abgebrochen. <br/>                                                              |
| <dl> <dt>**WIA \_ S KEIN GERÄT \_ \_ \_ VERFÜGBAR**</dt> </dl> | Keine WIA 2.0-Hardwaregeräte entsprechen den Im *lDeviceType-Parameter angegebenen* Spezifikationen. <br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode erstellt und zeigt das **Dialogfeld** Gerät auswählen an, damit der Benutzer ein WIA 2.0-Gerät für die Bilderfassung auswählen kann. Wenn ein Gerät erfolgreich ausgewählt wurde, erstellt die **IWiaDevMgr2::SelectDeviceDlg-Methode** eine hierarchische Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) für das Gerät. Er speichert einen Zeiger auf die **IWiaItem2-Schnittstelle** des Stammelements im *Parameter ppItemRoot*.

Die Anwendung kann die für den Benutzer angezeigten Geräte auf bestimmte Typen beschränken, indem sie die Gerätetypen über den *Parameter lDeviceType* angibt. Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2::SelectDeviceDlg** das Dialogfeld **Gerät** auswählen nicht an. Stattdessen wird die [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) für das Gerät erstellt und ein Zeiger auf die **IWiaItem2-Schnittstelle** des Stammelements im Parameter *ppItemRoot gespeichert.* Sie können dieses Verhalten außer Kraft setzen und **IWiaDevMgr2::SelectDeviceDlg** zwingen, das Dialogfeld anzuzeigen, indem Sie WIA SELECT DEVICE NODEFAULT als Wert für den \_ \_ \_ *lFlags-Parameter* angeben. Wenn mehr als ein WIA 2.0-Gerät der Spezifikation entspricht, werden alle übereinstimmenden Geräte im Dialogfeld Gerät auswählen angezeigt, damit der Benutzer eines auswählen kann. 

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenzeigen aufrufen, die sie über den *ppItemRoot-Parameter* erhalten.

> [!Note]  
> Es wird empfohlen, dass Anwendungen die Geräte- und Bildauswahl über ein Menüelement namens **From scanner** im Menü **Datei verfügbar** machen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
