---
description: Enthält Informationen über ein Lokalisier bares Druckformular.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: FORM_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215853"
---
# <a name="form_info_2-structure"></a>Formular \_ Info \_ 2-Struktur

Enthält Informationen über ein Lokalisier bares Druckformular.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Die Formular Eigenschaften. Die folgenden Werte sind definiert, aber es kann nur eine festgelegt werden. Wenn das **Formular \_ Info \_ 2** von [**GetForm**](getform.md) oder [**enumforms**](enumforms.md)zurückgegeben wird, wird **Flags** auf den aktuellen Wert in der Forms-Datenbank festgelegt.



| Wert         | Bedeutung                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formular \_ Benutzer    | Wenn dieses Bitflag festgelegt ist, wurde das Formular vom Benutzer definiert. Formulare mit diesem Flagsatz werden in der Registrierung definiert.                                                                                                                                                                    |
| Formular \_ vordefiniert | Wenn dieses Bitflag festgelegt ist, ist das Formular Teil des Spoolers. Formular Definitionen mit diesem Flagsatz werden nicht in der Registrierung angezeigt. Integrierte Formulare können nicht geändert werden. Daher sollte dieses Flag nicht festgelegt werden, wenn die Struktur an " [**AddForm**](addform.md) " oder " [**setform**](setform.md)" übermittelt wird. |
| Formular \_ Drucker | Wenn dieses Bitflag festgelegt ist, wird das Formular einem bestimmten Drucker zugeordnet, und seine Definition wird in der Registrierung angezeigt.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Formulars angibt. Der Formular Name darf nicht länger als 31 Zeichen sein.

</dd> <dt>

**Größe**
</dt> <dd>

Die Breite und Höhe des Formulars in tausendstel Millimeter.

</dd> <dt>

**Imageablearea**
</dt> <dd>

Die Breite und Höhe des Bereichs der Seite, auf der der Drucker drucken kann, in tausendstel Millimeter.

</dd> <dt>

**pkeyword**
</dt> <dd>

Ein Zeiger auf einen nicht lokalisierbaren Zeichen folgen Bezeichner des Formulars. Dies ermöglicht es dem Aufrufer, das Formular in allen Gebiets Schemas zu identifizieren, wenn es an [**AddForm**](addform.md) oder [**setform**](setform.md)übergeben wird.

</dd> <dt>

**StringType**
</dt> <dd>

Gibt an, wie ein lokalisierter Anzeige Name für das Formular zur Laufzeit abgerufen wird. Die folgenden Werte sind definiert. Nur eine kann in einem beliebigen Befehl von [**AddForm**](addform.md) oder [**setform**](setform.md)festgelegt werden. Sowohl String \_ muidll als auch String \_ langpair können in der **Form \_ Info \_ 2** (s) festgelegt werden, die von [**GetForm**](getform.md) oder [**enumforms**](enumforms.md)zurückgegeben wird. Siehe Hinweise.



| Wert            | Bedeutung                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zeichenfolge \_ None     | Es ist kein lokalisierter Anzeige Name vorhanden.                                                                                                                                                            |
| Zeichenfolge \_ muidll   | Der Anzeige Name wird von der in **pmuidll** angegebenen lokalisierten Ressourcen-DLL für die [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/mui-resource-management) extrahiert. Die ID befindet sich im Member **dwresourceid** . |
| Zeichenfolge \_ langpair | Der Anzeige Name und die Sprach-ID werden direkt von **pdisplayname** bereitgestellt, und die Sprache wird von **wlangid** angegeben.                                                                       |



 

</dd> <dt>

**pmuidll**
</dt> <dd>

Die [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/mui-resource-management) lokalisierte Ressourcen-DLL, die den lokalisierten anzeigen Amen enthält.

</dd> <dt>

**dwresourceid**
</dt> <dd>

Die Ressourcen-ID für den anzeigen amen des Formulars in **pmuidll**.

</dd> <dt>

**pdisplayname**
</dt> <dd>

Der Anzeige Name des Formulars in der Sprache, die von **wlangid** angegeben wird.

</dd> <dt>

**wlangid**
</dt> <dd>

Die Sprache von **pdisplayname**.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei einem Aufrufen von [**AddForm**](addform.md) oder [**setform**](setform.md):

-   Wenn **StringType** String \_ None ist, müssen sowohl **pmuidll** als auch **pdisplayname** **null** sein, und sowohl **dwresourceid** als auch **wlangid** müssen den Wert 0 aufweisen.
-   Wenn **StringType** String \_ muidll ist, muss **pdisplayname** **null** sein, und **wlangid** muss den Wert 0 aufweisen.
-   Wenn **StringType** "String \_ langpair" ist, muss **pmuidll** **null** sein, und " **dwresourceid** " muss den Wert "0" aufweisen.

Für ein **Formular \_ Info \_ 2** , das durch einen [**GetForm**](getform.md) -oder [**enumforms**](enumforms.md)-Rückruf zurückgegeben wird:

-   Wenn **StringType** sowohl String \_ muidll als auch String \_ langpair, **pmuidll**, **pdisplayname**, **dwresourceid** ist, **und wlangid** hat alle gültige Werte.
-   Wenn **StringType** nur String \_ muidll ist, verfügen **pmuidll** und **dwresourceid** über gültige Werte. **pdisplayname** ist **null** , und **wlangid** ist 0.
-   Wenn **StringType** nur String \_ langpair ist, verfügen **pdisplayname** und **wlangid** über gültige Werte. **pmuidll** ist **null** , und **dwresourceid** ist 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Formular \_ Info \_ 2W** (Unicode) und **\_ Formular \_ Info \_ 2a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[Multilingual User Interface](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**Enumforms**](enumforms.md)
</dt> <dt>

[**Setform**](setform.md)
</dt> </dl>

 

