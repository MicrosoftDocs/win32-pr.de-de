---
description: Enthält Informationen über das Dialogfeld, das von der CryptUIDlgSelectCertificate-Funktion angezeigt wird.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: CRYPTUI_SELECTCERTIFICATE_STRUCT Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f8cc80f740e26ac2d067705c9aac9aee387b91e28cb057366587375c874ae0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768234"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>STRUKTUR DER CRYPTUI \_ \_ SELECTCERTIFICATE-STRUKTUR

Die **Struktur CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT** enthält Informationen über das Dialogfeld, das von der [**CryptUIDlgSelectCertificate-Funktion**](cryptuidlgselectcertificate.md) angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Die Größe (in Bytes) dieser Struktur.

</dd> <dt>

**hwndParent**
</dt> <dd>

Das Handle des übergeordneten Fensters des Dialogfelds. Wenn dieser Wert **NULL** ist, ist das übergeordnete Fenster das Standarddesktopfenster.

</dd> <dt>

**dwFlags**
</dt> <dd>

Gibt zusätzliche Optionen für die [**CryptUIDlgSelectCertificate-Funktion**](cryptuidlgselectcertificate.md) an. Dies kann null oder ein bitweises **OR** der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt> </dl>                              | Reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ LEGACY**</dt> </dl>                                       | Gibt an, dass das Legacydialogfeld angezeigt werden soll.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ MULTISELECT**</dt> </dl>                        | Ermöglicht dem Benutzer, mehrere Zertifikate im Dialogfeld auszuwählen. Wenn dieses Flag festgelegt ist, gibt die [**CryptUIDlgSelectCertificate-Funktion**](cryptuidlgselectcertificate.md) immer **NULL** zurück. Der **hSelectedCertStore-Member** dieser Struktur muss ein Handle für einen Zertifikatspeicher enthalten. Die vom Benutzer ausgewählten Zertifikate werden diesem Speicher hinzugefügt.<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ PUT \_ WINDOW \_ TOPMOST**</dt> </dl> | Erzwingt, dass die Kryptografie-Benutzeroberfläche das obere Fenster auf dem Bildschirm ist.<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**szTitle**
</dt> <dd>

Der Anzeigetitel für das Dialogfeld. Wenn der Wert dieses Members **NULL** ist, wird der Standardtitel "Zertifikat auswählen" verwendet.

</dd> <dt>

**dwDontUseColumn**
</dt> <dd>

Flags, die kombiniert werden können, um Spalten der Anzeige auszuschließen.



| Wert                                                                                                                                                                                                                                                                                       | Bedeutung                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ ISSUEDTO \_ COLUMN**</dt> <dt>1 (0x1)</dt> </dl>             | Zeigen Sie keine **ISSUEDTO-Informationen an.**<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ ISSUEDBY \_ COLUMN**</dt> <dt>2 (0x2)</dt> </dl>             | Zeigen Sie keine **ISSUEDBY-Informationen** an.<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ INTENDEDUSE \_ COLUMN**</dt> <dt>4 (0x4)</dt> </dl>    | Zeigen Sie keine **IntendedUse-Informationen** an.<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ FRIENDLYNAME \_ COLUMN**</dt> <dt>8 (0x8)</dt> </dl> | Zeigen Sie keine Namensinformationen an.<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ LOCATION \_ COLUMN**</dt> <dt>16 (0x10)</dt> </dl>           | Zeigen Sie keine Standortinformationen an.<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ EXPIRATION \_ COLUMN**</dt> <dt>32 (0x20)</dt> </dl>     | Es werden keine Ablaufinformationen angezeigt.<br/>      |



 

</dd> <dt>

**szDisplayString**
</dt> <dd>

Text, der im Dialogfeld angezeigt wird, um den Benutzer anzuweisen. Wenn der Wert dieses Members **NULL** ist, wird die Standardzeichenfolge "Wählen Sie ein Zertifikat aus, das Sie verwenden möchten" verwendet.

</dd> <dt>

**pFilterCallback**
</dt> <dd>

Ein Zeiger auf eine [**PFNCFILTERPROC-Rückruffunktion,**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) die die im Dialogfeld angezeigten Zertifikate filtert.

</dd> <dt>

**pDisplayCallback**
</dt> <dd>

Ein Zeiger auf eine [**PFNCCERTDISPLAYPROC-Rückruffunktion,**](pfnccertdisplayproc.md) die Zertifikate anzeigt, die der Benutzer zur Anzeige auswählt.

</dd> <dt>

**pvCallbackData**
</dt> <dd>

Zusätzliche Daten, die an die rückruffunktionen übergeben werden, die von den **Membern pFilterCallback** und **pDisplayCallback** angegeben werden.

</dd> <dt>

**cDisplayStores**
</dt> <dd>

Die Anzahl der Zertifikatspeicher im **Array rghDisplayStores.**

</dd> <dt>

**rghDisplayStores**
</dt> <dd>

Ein Zeiger auf ein Array von Speichern, die zertifikate enthalten, die im Dialogfeld ausgewählt werden können.

</dd> <dt>

**cStores**
</dt> <dd>

Die Anzahl der Zertifikatspeicher im **Array rghStores.**

</dd> <dt>

**rghStores**
</dt> <dd>

Ein Zeiger auf ein Array von Zertifikatspeichern, die beim Erstellen einer Zertifikatkette und beim Überprüfen der Vertrauensstellung nach den im Dialogfeld angezeigten Zertifikaten durchsucht werden sollen.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

Die Anzahl der Eigenschaftenseiten im **rgPropSheetPages-Array.**

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Ein Zeiger auf ein Array von **PROPSHEETPAGE-Strukturen,** die Eigenschaftenseiten darstellen, die an das Dialogfeld zum Anzeigen des Zertifikats übergeben werden, wenn ein Zertifikat zum Anzeigen ausgewählt wird.

</dd> <dt>

**hSelectedCertStore**
</dt> <dd>

Ein Handle für einen vom Aufrufer erstellten Zertifikatspeicher. Die vom Benutzer ausgewählten Zertifikate werden diesem Speicher hinzugefügt. Wenn die Anzahl der Zertifikate in diesem Speicher vor und nach dem Aufruf von [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)gleich ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.

Dieser Member wird nicht verwendet, wenn der **dwFlags-Member** dieser Struktur das **CRYPTUI \_ SELECTCERT \_ MULTISELECT-Flag** nicht enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                            |
| Unicode- und ANSI-Name<br/>   | **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) und **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




