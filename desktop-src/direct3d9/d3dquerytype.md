---
description: Identifiziert den Abfragetyp.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: D3DQUERYTYPE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7a9c20050e7d0dce5a19664d937c016a475a9a13
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343075"
---
# <a name="d3dquerytype-enumeration"></a>D3DQUERYTYPE-Enumeration

Identifiziert den Abfragetyp. Informationen zu Abfragen finden Sie unter [Abfragen (Direct3D 9).](queries.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**
</dt> <dd>

Abfragen von Treiberhinweisen zum Datenlayout für die Scheitelpunktzwischenspeicherung.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

Fragen Sie den Ressourcen-Manager ab. Für diese Abfrage müssen die Geräteverhaltensflags [D3DCREATE \_ DISABLE DRIVER MANAGEMENT \_ \_ enthalten.](d3dcreate.md)

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**
</dt> <dd>

Abfragen von Scheitelpunktstatistiken.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE-EREIGNIS \_**
</dt> <dd>

Fragen Sie alle asynchronen Ereignisse ab, die von API-Aufrufen ausgegeben wurden.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ OCCLUSION**
</dt> <dd>

Eine Okklusionsabfrage gibt die Anzahl der Pixel zurück, die Z-Tests bestehen. Diese Pixel gelten für Primitive, die zwischen dem Problem [**von D3DISSUE \_ BEGIN**](d3dissue-begin.md) und [**D3DISSUE \_ END gezeichnet werden.**](d3dissue-end.md) Dadurch kann eine Anwendung das Okklusionsergebnis mit 0 (0) überprüfen. Null ist vollständig okkludent, was bedeutet, dass die Pixel von der aktuellen Kameraposition aus nicht sichtbar sind.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ TIMESTAMP**
</dt> <dd>

Gibt einen 64-Bit-Zeitstempel zurück.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**
</dt> <dd>

Verwenden Sie diese Abfrage, um eine Anwendung zu benachrichtigen, wenn sich die Zählerhäufigkeit von D3DQUERYTYPE \_ TIMESTAMP geändert hat.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**
</dt> <dd>

Dieses Abfrageergebnis ist **TRUE,** wenn nicht garantiert werden kann, dass die Werte aus D3DQUERYTYPE \_ TIMESTAMP-Abfragen während der gesamten Dauer der D3DQUERYTYPE \_ TIMESTAMPDISJOINT-Abfrage kontinuierlich sind. Andernfalls lautet das Abfrageergebnis **FALSE.**

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**
</dt> <dd>

Prozentsatz der Zeit, die Pipelinedaten verarbeitet.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**
</dt> <dd>

Prozentsatz der Zeit, die Daten im Treiber verarbeitet.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**
</dt> <dd>

Prozentsatz der Zeit für die Verarbeitung von Vertex-Shaderdaten.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**
</dt> <dd>

Prozentsatz der Zeit für die Verarbeitung von Pixel-Shaderdaten.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**
</dt> <dd>

Vergleiche der Durchsatzmessung zum Besseren des Verständnisses der Leistung einer Anwendung.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**
</dt> <dd>

Messen Sie die Cachetrefferratenleistung für Texturen und indizierte Scheitelpunkte.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**
</dt> <dd>

Effizienz der Speicherbelegung in einer [**D3DMEMORYPRESSURE-Struktur.**](d3dmemorypressure.md)

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- D3DQUERYTYPE MEMORYPRESSURE ist nur in Direct3D9Ex verfügbar, das unter \_ Windows 7 (oder mehr aktuellem Betriebssystem) ausgeführt wird.



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
