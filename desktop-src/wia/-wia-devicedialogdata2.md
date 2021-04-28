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
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089804"
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

Gibt die Dateinamenvorlage an, die für Dateien verwendet werden soll, die von WIA-Elementen in den durch **bstrFolderName festgelegten Zielordner übertragen werden.** Eine beliebige Anzahl eindeutiger Dateinamen kann durch Anfügen zusätzlicher Zeichen an die Dateinamenvorlage erstellt werden.

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

Zeiger auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des WIA-Elements, das Daten in die Datei oder dateien überträgt, die im **pbstrFilePaths-Array benannt** sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




