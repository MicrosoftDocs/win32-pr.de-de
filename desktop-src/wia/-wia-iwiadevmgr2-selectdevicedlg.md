---
description: Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2:: SelectDeviceDlg-Methode (WIA. h)'
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
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358465"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>IWiaDevMgr2:: SelectDeviceDlg-Methode

Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.

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

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Gibt das übergeordnete Fenster des Dialog Felds **Gerät auswählen** an.

</dd> <dt>

*LDE vicetype* \[ in\]
</dt> <dd>

Type: **Long**

Gibt an, welcher Typ von WIA 2,0-Gerät verwendet werden soll. Eine Liste der möglichen Werte finden Sie unter [WIA Device Type specifier](-wia-wia-device-type-specifiers.md) .

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt das Verhalten des Dialog Felds an. Der Wert kann einer der folgenden Werte sein:

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Verwendet das Standardverhalten.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ Select \_ Device \_ NODEFAULT**


</dt> <dd>

Zeigt das Dialogfeld an, obwohl nur ein entsprechendes Gerät vorhanden ist.

</dd> </dl> </dd> <dt>

*pbstraude viceid* \[ in, out\]
</dt> <dd>

Geben Sie Folgendes ein: **BSTR \** _

Bei der Ausgabe empfängt eine Zeichenfolge, die die Bezeichnerzeichenfolge des Geräts enthält. Übergeben Sie bei der Eingabe die Adresse eines Zeigers, wenn diese Informationen benötigt werden, oder _ *null**, wenn er nicht benötigt wird.

</dd> <dt>

*ppitemroot* \[ Out, retval\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements der hierarchischen Struktur, die das ausgewählte WIA 2,0-Gerät darstellt. Wenn kein Gerät gefunden wird, wird **null** empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                  | Beschreibung                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Das Gerät wurde erfolgreich ausgewählt. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | Der Benutzer hat das Dialogfeld abgebrochen. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ kein \_ Gerät \_ verfügbar**</dt> </dl> | Keine WIA 2,0-Hardware Geräte entsprechen den Spezifikationen im *ldebug Type* -Parameter. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird das Dialogfeld **Gerät auswählen** erstellt und angezeigt, sodass der Benutzer ein WIA 2,0-Gerät für die Abbild Erfassung auswählen kann. Wenn ein Gerät erfolgreich ausgewählt wurde, erstellt die **IWiaDevMgr2:: SelectDeviceDlg** -Methode eine hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten für das Gerät. Es speichert einen Zeiger auf die **IWiaItem2** -Schnittstelle des Stamm Elements im Parameter *ppitemroot*.

Die Anwendung kann die Geräte, die dem Benutzer angezeigt werden, auf bestimmte Typen beschränken, indem Sie die Gerätetypen über den *ltovicetype* -Parameter angeben. Wenn nur ein Gerät der Spezifikation entspricht, wird von **IWiaDevMgr2:: selectde vicedlg** das Dialogfeld **Gerät auswählen** nicht angezeigt. Stattdessen wird die [**IWiaItem2**](-wia-iwiaitem2.md) -Struktur für das Gerät erstellt und ein Zeiger auf die **IWiaItem2** -Schnittstelle des Stamm Elements im Parameter *ppitemroot* gespeichert. Sie können dieses Verhalten überschreiben und **IWiaDevMgr2:: SelectDeviceDlg** erzwingen, um das Dialogfeld anzuzeigen, indem Sie WIA \_ Select \_ Device \_ NODEFAULT als Wert für den *lFlags* -Parameter angeben. Wenn mehr als ein WIA 2,0-Gerät mit der Spezifikation übereinstimmt, werden alle übereinstimmenden Geräte im Dialogfeld **Gerät auswählen** angezeigt, sodass der Benutzer eine Auswahl treffen kann.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppitemroot* -Parameter empfangen.

> [!Note]  
> Es wird empfohlen, dass Anwendungen die Geräte-und Abbild Auswahl über ein Menü Element namens **von Scanner** im Menü **Datei** verfügbar machen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
