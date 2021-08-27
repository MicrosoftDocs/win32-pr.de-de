---
description: Rückruf zum Zurückgeben von Objekttabellendaten.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 81d5533e5015d532ea7186dbd81321d9d42bb418
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622486"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback-Schnittstelle

Rückruf zum Zurückgeben von Objekttabellendaten.

## <a name="members"></a>Member

Die **IObjectTableCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IObjectTableCallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **IObjectTableCallback-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">Methode</th><th style="text-align: left;">Beschreibung</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></td><td style="text-align: left;"><p>Ruft Informationen darüber ab, welche Spalten (Objektdatentypen) von der Objekttabelle unterstützt werden.</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>Eine Rückruffunktion, die verwendet wird, um den Host von Objekttabelleninformationen zu benachrichtigen.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
