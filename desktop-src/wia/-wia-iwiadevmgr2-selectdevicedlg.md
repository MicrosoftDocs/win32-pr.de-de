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
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091258"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>IWiaDevMgr2::SelectDeviceDlg-Methode

Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardwaregerät für die Imageerfassung auswählen kann.

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

Gibt das übergeordnete Fenster des Dialogfelds **Gerät auswählen** an.

</dd> <dt>

*lDeviceType* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt an, welcher WiA 2.0-Gerätetyp verwendet werden soll. Eine Liste der möglichen Werte finden Sie unter [WIA-Gerätetypspezifizierer.](-wia-wia-device-type-specifiers.md)

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt das Verhalten des Dialogfelds an. Der Wert kann einer der folgenden Sein:

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Verwendet das Standardverhalten.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**


</dt> <dd>

Zeigt das Dialogfeld an, obwohl nur ein übereinstimmendes Gerät vorhanden ist.

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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt und zeigt das **Dialogfeld Gerät** auswählen an, damit der Benutzer ein WIA 2.0-Gerät für die Bilderfassung auswählen kann. Wenn ein Gerät erfolgreich ausgewählt wurde, erstellt die **IWiaDevMgr2::SelectDeviceDlg-Methode** eine hierarchische Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) für das Gerät. Er speichert einen Zeiger auf die **IWiaItem2-Schnittstelle** des Stammelements im *Parameter ppItemRoot*.

Die Anwendung kann die dem Benutzer angezeigten Geräte auf bestimmte Typen beschränken, indem sie die Gerätetypen über den *Parameter lDeviceType* angibt. Wenn nur ein Gerät die Spezifikation erfüllt, zeigt **IWiaDevMgr2::SelectDeviceDlg** das Dialogfeld **Gerät** auswählen nicht an. Stattdessen wird die [**IWiaItem2-Struktur**](-wia-iwiaitem2.md) für das Gerät erstellt und ein Zeiger auf die **IWiaItem2-Schnittstelle** des Stammelements im Parameter *ppItemRoot gespeichert.* Sie können dieses Verhalten überschreiben und **IWiaDevMgr2::SelectDeviceDlg** zwingen, das Dialogfeld anzuzeigen, indem Sie WIA SELECT DEVICE NODEFAULT als Wert für den \_ \_ \_ *lFlags-Parameter* angeben. Wenn mehr als ein WIA 2.0-Gerät mit der Spezifikation übereinstimmt, werden alle übereinstimmenden Geräte im Dialogfeld **Gerät auswählen** angezeigt, damit der Benutzer eines auswählen kann.

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Schnittstellenzeiger aufrufen, die sie über den *ppItemRoot-Parameter* empfangen.

> [!Note]  
> Es wird empfohlen, dass Anwendungen die Geräte- und Bildauswahl über ein Menüelement mit dem Namen **Von Scanner** im Menü **Datei** verfügbar machen.

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
