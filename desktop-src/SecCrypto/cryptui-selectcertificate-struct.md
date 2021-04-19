---
description: Enthält Informationen über das Dialogfeld, das von der cryptuidlgselectcertificate-Funktion angezeigt wird.
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
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355395"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>Cryptui \_ selectcertificate- \_ Struktur Struktur

Die **cryptui \_ selectcertificate \_** -Struktur Struktur enthält Informationen zu dem Dialogfeld, das von der [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) -Funktion angezeigt wird.

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

Das Handle des übergeordneten Fensters des Dialog Felds. Wenn dieser Wert **null** ist, ist das übergeordnete Fenster das Standard Desktop Fenster.

</dd> <dt>

**dwFlags**
</dt> <dd>

Gibt zusätzliche Optionen für die [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) -Funktion an. Dies kann NULL oder ein bitweises **or** der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**cryptui \_ selectcert \_ addfromds**</dt> </dl>                              | Reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**cryptui \_ selectcert- \_ Legacy**</dt> </dl>                                       | Gibt an, dass das Legacy Dialogfeld angezeigt werden soll.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**cryptui \_ selectcert \_ MultiSelect**</dt> </dl>                        | Ermöglicht es dem Benutzer, mehr als ein Zertifikat im Dialogfeld auszuwählen. Wenn dieses Flag festgelegt ist, gibt die Funktion [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md) immer **null** zurück. Der **hselectedcertstore** -Member dieser Struktur muss ein Handle für einen Zertifikat Speicher enthalten. Die Zertifikate, die vom Benutzer ausgewählt werden, werden diesem Speicher hinzugefügt.<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**cryptui \_ selectcert \_ Put \_ Window \_ Top**</dt> </dl> | Erzwingt, dass die kryptografiebenutzeroberfläche das oberste Fenster auf dem Bildschirm ist.<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**sztitle**
</dt> <dd>

Der Anzeige Titel für das Dialogfeld. Wenn der Wert dieses Members **null** ist, wird der Standard Titel "Zertifikat auswählen" verwendet.

</dd> <dt>

**dwdontusecolumn**
</dt> <dd>

Flags, die kombiniert werden können, um Spalten der Anzeige auszuschließen.



| Wert                                                                                                                                                                                                                                                                                       | Bedeutung                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**Cryptui \_ \_IssuedTo- \_ Spalte**</dt> <dt>1 (0x1)</dt> auswählen </dl>             | **IssuedTo** -Informationen nicht anzeigen.<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**Cryptui \_ Select \_ IssuedBy \_ Spalte**</dt> <dt>2 (0x2)</dt> </dl>             | **IssuedBy** -Informationen nicht anzeigen.<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**Cryptui \_ \_Intendeduse- \_ Spalte**</dt> <dt>4 (0x4)</dt> auswählen </dl>    | Zeigen Sie keine **intendeduse** -Informationen an.<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**Cryptui \_ Wählen Sie \_ FriendlyName \_ Column**</dt> <dt>8 (0x8)</dt> aus. </dl> | Zeigen Sie keine Namensinformationen an.<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**Cryptui \_ \_Location \_ Column**</dt> <dt>16 (0x10)</dt> auswählen </dl>           | Zeigen Sie keine Standortinformationen an.<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**Cryptui \_ \_Ablauf \_ Spalte**</dt> <dt>32 (0x20)</dt> auswählen </dl>     | Ablauf Informationen nicht anzeigen.<br/>      |



 

</dd> <dt>

**szdisplaystring**
</dt> <dd>

Text, der im Dialogfeld angezeigt wird, um den Benutzer anzuweisen. Wenn der Wert dieses Members **null** ist, wird die Standard Zeichenfolge "wählen Sie ein Zertifikat aus, das Sie verwenden möchten" verwendet.

</dd> <dt>

**pfiltercallback**
</dt> <dd>

Ein Zeiger auf eine [**pfncfilterproc**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) -Rückruffunktion, die die Zertifikate filtert, die im Dialogfeld angezeigt werden.

</dd> <dt>

**pdisplaycallback**
</dt> <dd>

Ein Zeiger auf eine [**pfnccertdisplayproc**](pfnccertdisplayproc.md) -Rückruffunktion, die Zertifikate anzeigt, die der Benutzer zum anzeigen auswählt.

</dd> <dt>

**pvcallbackdata**
</dt> <dd>

Zusätzliche Daten, die an die Rückruf Funktionen übergeben werden, die von den **pfiltercallback** -und **pdisplaycallback** -Membern angegeben werden.

</dd> <dt>

**cdisplaystores**
</dt> <dd>

Die Anzahl der Zertifikat Speicher im **rghdisplaystores** -Array.

</dd> <dt>

**rghdisplaystores**
</dt> <dd>

Ein Zeiger auf ein Array von Stores, die Zertifikate enthalten, die im Dialogfeld zur Auswahl stehen.

</dd> <dt>

**cstores**
</dt> <dd>

Die Anzahl der Zertifikat Speicher im **rghstores** -Array.

</dd> <dt>

**rghstores**
</dt> <dd>

Ein Zeiger auf ein Array von Zertifikat speichern, das beim Aufbau einer Zertifikat Kette durchsucht werden soll, und das Überprüfen der Vertrauenswürdigkeit für die im Dialogfeld angezeigten Zertifikate.

</dd> <dt>

**cpropsheetpages**
</dt> <dd>

Die Anzahl der Eigenschaften Seiten im **rgpropsheetpages** -Array.

</dd> <dt>

**rgpropsheetpages**
</dt> <dd>

Ein Zeiger auf ein Array von **PROPSHEETPAGE** -Strukturen, die Eigenschaften Seiten darstellen, die an das Dialogfeld zum Anzeigen von Zertifikaten übermittelt werden, wenn ein Zertifikat für die Anzeige ausgewählt wird.

</dd> <dt>

**hselectedcertstore**
</dt> <dd>

Ein Handle für einen vom Aufrufer erstellten Zertifikat Speicher. Die vom Benutzer ausgewählten Zertifikate werden diesem Speicher hinzugefügt. Wenn die Anzahl der Zertifikate in diesem Speicher vor und nach dem Aufruf von [**cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md)identisch ist, hat der Benutzer das Dialogfeld geschlossen, ohne Zertifikate auszuwählen.

Dieser Member wird nicht verwendet, wenn der **dwFlags** -Member dieser Struktur das MultiSelect-Flag " **cryptui \_ selectcert \_** " nicht enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                            |
| Unicode- und ANSI-Name<br/>   | **Cryptui \_ Selectcertificate \_ structw** (Unicode) und **cryptui \_ selectcertificate \_ Structa** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cryptuidlgselectcertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




