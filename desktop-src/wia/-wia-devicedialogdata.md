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
ms.openlocfilehash: e20b8689e71031024c46451d3079450061e8112acf1052c12129b89ed9e0a23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451200"
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
| \_WIA-GERÄTEDIALOGFELD \_ \_ – \_ EINZELBILD   | Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld zum Erfassen von Geräteimages.                                                                                                      |
| \_WIA DEVICE \_ DIALOG USE COMMON UI (WIA-GERÄTEDIALOGFELD: \_ ALLGEMEINE \_ BENUTZEROBERFLÄCHE VERWENDEN) \_ | Verwenden Sie ggf. die Systembenutzeroberfläche anstelle der vom Anbieter bereitgestellten Benutzeroberfläche. Wenn die Systemoberfläche nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet. Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ NOTIMPL zurück. |



 

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



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




