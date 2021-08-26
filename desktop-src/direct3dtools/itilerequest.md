---
description: Fordern Sie an, dass eine gekachelte Textur als DDS-Datei geschrieben wird.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITileRequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0a5f31e68f53f316ea77f77f2ff778eb817e11c
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786166"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span id="vspixengine.itilerequest"></span>ITileRequest-Schnittstelle

Fordern Sie an, dass eine gekachelte Textur als DDS-Datei geschrieben wird.

## <a name="members"></a>Members

Die **ITileRequest-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITileRequest** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Methoden

Die **ITileRequest-Schnittstelle** verfügt über diese Methoden.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Methode</th><th >BESCHREIBUNG</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></td><td ><p>Fordert an, den Rohdateninhalt einer Kachel abzurufen.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></td><td ><p>Fordert an, den Inhalt einer gekachelten Textur als abzurufen. DDS-Datei (DirectDraw Surface).</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Anforderungen

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
