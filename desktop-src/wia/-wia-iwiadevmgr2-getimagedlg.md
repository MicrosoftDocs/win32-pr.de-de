---
description: Die IWiaDevMgr2::GetImageDlg-Methode zeigt mindestens ein Dialogfeld an, mit dem ein Benutzer ein Bild von einem WIA 2.0-Gerät (Windows Image Acquisition) erwerben und in eine angegebene Datei schreiben kann.
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: IWiaDevMgr2::GetImageDlg-Methode (Wia.h)
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
ms.openlocfilehash: 0b03356e40f1c708c852917c890e4c1bf96b98cd18ccf82b75ebcaaccaa69597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814040"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>IWiaDevMgr2::GetImageDlg-Methode

Die **IWiaDevMgr2::GetImageDlg-Methode** zeigt ein oder mehrere Dialogfelder an, die es einem Benutzer ermöglichen, ein Bild von einem WIA 2.0-Gerät (Windows Image Acquisition) zu erhalten und es in eine angegebene Datei zu schreiben. Diese Methode erweitert die Funktionalität von [**IWiaDevMgr2::SelectDeviceDlg,**](-wia-iwiadevmgr2-selectdevicedlg.md) um die Bilderfassung innerhalb eines einzelnen API-Aufrufs zu kapseln.

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

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt das Verhalten des Dialogfelds an. Kann auf die folgenden Werte festgelegt werden:



| Flag                                 | Bedeutung                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Standardverhalten.                                                                                                                                                           |
| DIALOGFELD \_ "WIA-GERÄT" \_ VERWENDEN DER ALLGEMEINEN \_ \_ \_ BENUTZEROBERFLÄCHE | Verwenden Sie die Systembenutzeroberfläche anstelle der vom Anbieter bereitgestellten Benutzeroberfläche. Wenn die Systembenutzeroberfläche nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet. Wenn keine der Benutzeroberflächen verfügbar ist, gibt die Funktion E \_ NOTIMPL zurück. |



 

</dd> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den zu verwendenden Scanner an.

</dd> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Ein Handle des Fensters, das das **Dialogfeld Bild herunterladen** besitzt.

</dd> <dt>

*bstrFolderName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen des Ordners an, in dem die gescannten Dateien gespeichert werden.

</dd> <dt>

*bstrFilename* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Datei an, in die die Bilddaten geschrieben werden.

</dd> <dt>

*plNumFiles* \[ In\]
</dt> <dd>

Typ: **\* LONG**

Ein Zeiger auf die Anzahl der zu überprüfenden Dateien.

</dd> <dt>

*ppbstrFilePaths* \[ In\]
</dt> <dd>

Typ: **BSTR \* \***

Die Adresse eines Zeigers auf ein Array von Pfaden für die gescannten Dateien. Initialisieren Sie den Zeiger, um auf ein Array der Größe 0 (null) zu zeigen, bevor **IWiaDevMgr2::GetImageDlg** aufgerufen wird. Siehe **Hinweise**.

</dd> <dt>

*ppItem* \[ in, out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Die Adresse eines Zeigers auf [**IWiaItem2,**](-wia-iwiaitem2.md) von dem die Bilder gescannt wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

**IWiaDevMgr2::GetImageDlg** gibt S OK zurück, wenn die Daten erfolgreich übertragen wurden, gibt S FALSE zurück, wenn der Benutzer das Dialogfeld abbricht, oder gibt einen COM-Standardfehler \_ \_ zurück.

> [!Note]  
> Der *ppbstrFilePaths-Parameter* ist nicht unbedingt leer, wenn die Funktion S \_ FALSE zurückgibt. Wenn der Benutzer abbricht, werden die Seiten, die die Überprüfung abgeschlossen haben, verarbeitet und in *ppbstrFilePaths zurückgegeben.* Auch wenn sie nicht verwendet werden, müssen Sie das Array frei geben. Siehe **Hinweise**.

 

## <a name="remarks"></a>Hinweise

Wenn die Anwendung **NULL** für den Wert des *Parameters bstrDeviceID* übergibt, zeigt **IWiaDevMgr2::GetImageDlg** das Dialogfeld Gerät auswählen an, damit der Benutzer das WIA 2.0-Eingabegerät auswählen kann. 

Verwenden Sie ein Menüelement mit dem Namen **From scanner** im Menü **Datei,** damit die Geräte- und Bildauswahl in Ihrer Anwendung verfügbar ist.

Rufen [Sie SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) für jeden BSTR im Array auf, auf das *ppbstrFilePaths* i zeigt, und rufen Sie \[ \] [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) für das Array selbst auf, um zugeordneten Arbeitsspeicher frei zu geben. Wenn S FALSE zurückgegeben wird, überprüfen Sie, ob der Wert, auf \_ *den plNumFiles* zeigt, nicht 0 (null) ist. Wenn der Wert nicht 0 (null) ist, geben Sie die *ppbstrFilePaths* i-Ressourcen in der Anwendung frei, da der Benutzer nach dem Scannen einer oder mehrere Seiten \[ \] abbrechen kann. Initialisieren *Sie plNumFiles auf* 0 (null), bevor **Sie IWiaDevMgr2::GetImageDlg aufrufen.** Wenn *plNumFiles* nicht mit 0 initialisiert wird und ein Fehler in der COM-Infrastruktur bewirkt, dass die Funktion S FALSE zurück gibt, bevor \_ **IWiaDevMgr2::GetImageDlg** aufgerufen wird, hat *plNumFiles* einen irreführenden Garbage Value.

Das Dialogfeld muss über ausreichende Rechte für *bstrFolderName* verfügen, damit die Dateien mit eindeutigen Dateinamen gespeichert werden können. Schützen Sie den Ordner mit einer Zugriffssteuerungsliste (Access Control List, ACL), da er Benutzerdaten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 
