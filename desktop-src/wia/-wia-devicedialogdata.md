---
description: 'DEVICEDIALOGDATA-Struktur: Definiert die Daten, die zum Aufrufen eines Gerätedialogs erforderlich sind.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: DEVICEDIALOGDATA-Struktur (Wiadefd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: ad7b08f5396a7a6e9b1f74df3dd409303b2d548d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104268"
---
# <a name="devicedialogdata-structure"></a>DEVICEDIALOGDATA-Struktur

Definiert die Daten, die zum Aufrufen eines Gerätedialogfelds erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt die Größe dieser Struktur in Bytes an.

</dd> <dt>

**hwndParent**
</dt> <dd>

Typ: **HWND**

</dd> <dd>

Gibt das Handle für das übergeordnete Fenster des Dialogfelds an.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Typ: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***

</dd> <dd>

Zeigt auf eine [**IWiaItem-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) die das gültige Stammelement in der Anwendungselementstruktur darstellt.

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

**lIntent**
</dt> <dd>

Typ: **LONG**

</dd> <dd>

Gibt an, welche Art von Daten das Bild darstellen soll. Eine Liste der Bildabsichtwerte finden Sie unter [**Bildabsichtkonstanten.**](-wia-imageintentconstants.md)

</dd> <dt>

**lItemCount**
</dt> <dd>

Typ: **LONG**

</dd> <dd>

Empfängt die Anzahl der Elemente im Array, die durch den **ppWiaItem-Parameter** angegeben werden.

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Typ: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Empfängt die Adresse eines Arrays von Zeigern auf [**IWiaItem-Schnittstellen.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




