---
description: Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: DEVICEDIALOGDATA2-Struktur (wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042283"
---
# <a name="devicedialogdata2-structure"></a>DEVICEDIALOGDATA2-Struktur

Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt die Größe dieser Struktur in Bytes an.

</dd> <dt>

**piwiaitemroot**
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

Verweist auf eine [_ *IWiaItem2* *](-wia-iwiaitem2.md) -Schnittstelle, die das gültige Stamm Element in der Anwendungs Elementstruktur darstellt.

</dd> <dt>

**dwFlags**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt einen Satz von Flags an, die den Vorgang des Dialog Felds steuern. Kann auf einen der folgenden Werte festgelegt werden:



| Flag                                 | Bedeutung                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Standardverhalten.                                                                                                                                                                           |
| WIA- \_ Geräte \_ Dialogfeld, \_ einzelnes \_ Bild   | Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld Geräte Abbild Erfassung.                                                                                                      |
| Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche | Verwenden Sie die Benutzeroberfläche des Systems, falls verfügbar, anstelle der vom Hersteller bereitgestellten Benutzeroberfläche. Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet. Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück. |



 

</dd> <dt>

**hwndParent**
</dt> <dd>

Typ: **HWND**

</dd> <dd>

Gibt das Handle für das übergeordnete Fenster des Dialog Felds an.

</dd> <dt>

**bstrinfoldername**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Gibt den Ordnernamen an, in den die Dateien übertragen werden.

</dd> <dt>

**bstrFilename**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Gibt die Dateinamen Vorlage an, die für Dateien verwendet werden soll, die von WIA-Elementen in den von **bstrindername** festgelegten Zielordner übertragen werden. Eine beliebige Anzahl eindeutiger Dateinamen kann erstellt werden, indem zusätzliche Zeichen an die Dateinamen Vorlage angehängt werden.

</dd> <dt>

**lnumfiles**
</dt> <dd>

Type: **Long**

</dd> <dd>

Empfängt die Anzahl der Zeichen folgen, die in das **pbstrfilepath** -Array geschrieben werden.

</dd> <dt>

**pbstraufilepfade**
</dt> <dd>

Geben Sie Folgendes ein: **BSTR \** _

</dd> <dd>

Zeiger auf ein Array von BSTR-Zeigern. Jedes Array Element verweist auf ein BSTR, das den Zielnamen einer Datei enthält, die erfolgreich in den von bstrindername identifizierten Ordner übertragen wurde. Die-Methode muss den Speicher für diesen Member zuordnen.

</dd> <dt>

_ *ppwiaitem**
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

Ein Zeiger auf die [_ *IWiaItem2* *](-wia-iwiaitem2.md) -Schnittstelle des WIA-Elements, die Daten an die Datei oder die Dateien im **pbstrfilepath** -Array überträgt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




