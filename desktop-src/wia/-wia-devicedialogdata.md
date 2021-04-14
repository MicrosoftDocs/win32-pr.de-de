---
description: Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Devicedialogdata-Struktur (wiadefd. h)
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
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529156"
---
# <a name="devicedialogdata-structure"></a>Devicedialogdata-Struktur

Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.

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

**CBSIZE**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Gibt die Größe dieser Struktur in Bytes an.

</dd> <dt>

**hwndParent**
</dt> <dd>

Typ: **HWND**

</dd> <dd>

Gibt das Handle für das übergeordnete Fenster des Dialog Felds an.

</dd> <dt>

**piwiaitemroot**
</dt> <dd>

Typ: **[**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _

</dd> <dd>

Verweist auf eine [_ *iwiaitem* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle, die das gültige Stamm Element in der Anwendungs Elementstruktur darstellt.

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

**lintent**
</dt> <dd>

Type: **Long**

</dd> <dd>

Gibt an, welche Art von Daten das Image darstellen soll. Eine Liste der Abbild Intent-Werte finden Sie unter [**Bild beabsichtigte Konstanten**](-wia-imageintentconstants.md).

</dd> <dt>

**litemcount**
</dt> <dd>

Type: **Long**

</dd> <dd>

Empfängt die Anzahl von Elementen im Array, die durch den **ppwiaitem** -Parameter angegeben werden.

</dd> <dt>

**ppwiaitem**
</dt> <dd>

Typ: **[ **iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Empfängt die Adresse eines Arrays von Zeigern auf [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstellen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




