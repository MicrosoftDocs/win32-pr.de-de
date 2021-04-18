---
description: 'Die IWiaDevMgr2:: getimagedlg-Methode zeigt ein oder mehrere Dialogfelder an, mit denen ein Benutzer ein Bild von einem Windows-Image Erfassungsgerät (WIA) 2,0 abrufen und in eine angegebene Datei schreiben kann.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2:: getimagedlg-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359060"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>IWiaDevMgr2:: getimagedlg-Methode

Die **IWiaDevMgr2:: getimagedlg** -Methode zeigt ein oder mehrere Dialogfelder an, mit denen ein Benutzer ein Bild von einem Windows-Image Erfassungsgerät (WIA) 2,0 abrufen und in eine angegebene Datei schreiben kann. Mit dieser Methode wird die Funktionalität von [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) erweitert, um die Bild Erfassung innerhalb eines einzelnen API-Aufrufs zu kapseln.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt das Dialogfeld Verhalten an. Kann auf die folgenden Werte festgelegt werden:



| Flag                                 | Bedeutung                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Standardverhalten.                                                                                                                                                           |
| Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche | Verwenden Sie die Benutzeroberfläche des-Systems anstelle der vom Hersteller bereitgestellten Benutzeroberfläche. Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet. Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück. |



 

</dd> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den zu verwendenden Scanner an.

</dd> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein Handle des Fensters, das das Dialogfeld " **Bild Abbild** " besitzt.

</dd> <dt>

*bstrinfoldername* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen des Ordners an, in dem die gescannten Dateien gespeichert werden.

</dd> <dt>

*bstrauch filename* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Datei an, in die die Bilddaten geschrieben werden sollen.

</dd> <dt>

*plnumfiles* \[ in\]
</dt> <dd>

Type: **Long \** _

Ein Zeiger auf die Anzahl der zu überprüfenden Dateien.

</dd> <dt>

_ppbstrFilePaths * \[ in\]
</dt> <dd>

Typ: **BSTR \* \***

Die Adresse eines Zeigers auf ein Array von Pfaden für die gescannten Dateien. Initialisieren Sie den Zeiger so, dass er auf ein Array der Größe 0 (null) verweist, bevor **IWiaDevMgr2:: getimagedlg** aufgerufen wird. Siehe **Hinweise**.

</dd> <dt>

*ppitem* \[ in, out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Die Adresse eines Zeigers auf den [**IWiaItem2**](-wia-iwiaitem2.md) , von dem die Bilder gescannt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

**IWiaDevMgr2:: getimagedlg** gibt "s OK" zurück \_ , wenn die Daten erfolgreich übertragen werden, gibt "false" zurück, \_ Wenn der Benutzer das Dialogfeld abbricht, oder gibt einen com-Standardfehler zurück.

> [!Note]  
> Der *ppbstraufilepath* -Parameter ist nicht notwendigerweise leer, wenn die Funktion "S false" zurückgibt \_ . Wenn der Benutzer abbricht, werden die Seiten, bei denen die Überprüfung abgeschlossen ist, verarbeitet und in *ppbstraufilepath* zurückgegeben. Auch wenn Sie nicht verwendet werden, müssen Sie das Array freigeben. Siehe **Hinweise**.

 

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung für den Wert des Parameters *bstraude viceid* den Wert **null** übergibt, zeigt **IWiaDevMgr2:: getimagetimagedlg** das Dialogfeld **Gerät auswählen** an, sodass der Benutzer das WIA 2,0-Eingabegerät auswählen kann.

Verwenden Sie im Menü **Datei** ein Menü Element mit dem Namen **aus Scanner** , damit die Geräte-und Image Auswahl in der Anwendung verfügbar ist.

Nennen Sie [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) auf jedem BSTR im Array, auf das *ppbstraufilepath* \[ \] verweist, und nennen Sie " [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " für das Array selbst, um zugeordneten Arbeitsspeicher freizugeben. Wenn S \_ false zurückgegeben wird, überprüfen Sie, ob der Wert, auf den *plnumfiles* verweist, nicht NULL ist. Wenn der Wert nicht NULL ist, können Sie die Ressourcen von *ppbtrefilepath* \[ i \] in der Anwendung freigeben, da der Benutzer nach dem Scannen einer oder mehrerer Seiten abbrechen kann. Initialisieren Sie *plnumfiles* mit 0 (null), bevor Sie **IWiaDevMgr2:: getimagedlg** aufrufen. Wenn *plnumfiles* nicht mit 0 (null) initialisiert wird und ein Fehler in der com-Infrastruktur bewirkt, dass die Funktion den Wert "false" zurückgibt \_ , bevor **IWiaDevMgr2:: getimagedlg** aufgerufen wird, weist *plnumfiles* einen irreführenden Garbage-Wert auf.

Das Dialogfeld muss über ausreichende Berechtigungen für *bstrinfoldername* verfügen, damit die Dateien mit eindeutigen Dateinamen gespeichert werden können. Schützen Sie den Ordner mit einer Zugriffs Steuerungs Liste (Access Control List, ACL), da er Benutzerdaten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
