---
description: 'DEVICEDIALOGDATA2-Struktur: Definiert die Daten, die zum Aufrufen eines Gerätedialogs erforderlich sind.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: DEVICEDIALOGDATA2-Struktur (Wiadefd.h)
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
ms.openlocfilehash: 800f7ceb102cafcad8ddda5204990706b908a4a0137a16143af76a90345b472e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451190"
---
# <a name="devicedialogdata2-structure"></a>DEVICEDIALOGDATA2-Struktur

Definiert die Daten, die zum Aufrufen eines Gerätedialogfelds erforderlich sind.

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

**cbSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt die Größe dieser Struktur in Bytes an.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Zeigt auf eine [**IWiaItem2-Schnittstelle,**](-wia-iwiaitem2.md) die das gültige Stammelement in der Anwendungselementstruktur darstellt.

</dd> <dt>

**dwFlags**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt einen Satz von Flags an, die den Vorgang des Dialogfelds steuern. Kann auf einen der folgenden Werte festgelegt werden:



| Flag                                 | Bedeutung                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Standardverhalten.                                                                                                                                                                           |
| \_WIA-GERÄTEDIALOGFELD \_ \_ – \_ EINZELNES IMAGE   | Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld "Gerätebilderfassung".                                                                                                      |
| DIALOGFELD \_ "WIA-GERÄT" \_ VERWENDEN DER ALLGEMEINEN \_ \_ \_ BENUTZEROBERFLÄCHE | Verwenden Sie die Systembenutzeroberfläche (falls verfügbar) anstelle der vom Anbieter bereitgestellten Benutzeroberfläche. Wenn die Systembenutzeroberfläche nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet. Wenn keine der Benutzeroberflächen verfügbar ist, gibt die Funktion E \_ NOTIMPL zurück. |



 

</dd> <dt>

**hwndParent**
</dt> <dd>

Typ: **HWND**

</dd> <dd>

Gibt das Handle für das übergeordnete Fenster des Dialogfelds an.

</dd> <dt>

**bstrFolderName**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Gibt den Ordnernamen an, an den die Dateien übertragen werden.

</dd> <dt>

**bstrFilename**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Gibt die Dateinamenvorlage an, die für Dateien verwendet werden soll, die von WIA-Elementen in den durch **bstrFolderName festgelegten Zielordner übertragen werden.** Eine beliebige Anzahl eindeutiger Dateinamen kann erstellt werden, indem der Dateinamenvorlage zusätzliche Zeichen angefügt werden.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Typ: **LONG**

</dd> <dd>

Empfängt die Anzahl der Zeichenfolgen, die in das **pbstrFilePaths-Array geschrieben** werden.

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Typ: **BSTR \***

</dd> <dd>

Zeiger auf ein Array von BSTR-Zeigern. Jedes Arrayelement verweist auf einen BSTR, der den Zielnamen einer Datei enthält, die erfolgreich in den durch bstrFolderName identifizierten Ordner übertragen wurde. Die -Methode muss den Speicher für diesen Member zuordnen.

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Zeiger auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des WIA-Elements, das Daten an die Im **pbstrFilePaths-Array** benannte Datei überträgt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




