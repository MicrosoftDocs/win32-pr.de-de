---
description: Identifiziert den Abfragetyp.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: D3DQUERYTYPE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355021"
---
# <a name="d3dquerytype-enumeration"></a>D3DQUERYTYPE-Enumeration

Identifiziert den Abfragetyp. Weitere Informationen zu Abfragen finden Sie unter [Abfragen (Direct3D 9)](queries.md) .

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

Fragen Sie Treiber Hinweise zum Datenlayout für Scheitelpunkt Caching ab.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

Fragen Sie den Ressourcen-Manager ab. Für diese Abfrage müssen die geräteverhaltenflags [D3DCREATE \_ deaktivierte \_ Treiber \_ Verwaltung](d3dcreate.md)einschließen.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ vertexstats**
</dt> <dd>

Abfragen von Vertex-Statistiken.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE- \_ Ereignis**
</dt> <dd>

Fragen Sie alle asynchronen Ereignisse ab, die von API-aufrufen ausgegeben wurden.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE- \_ oksion**
</dt> <dd>

Eine oksions Abfrage gibt die Anzahl der Pixel zurück, die z-Tests bestehen. Diese Pixel sind für primitive, die zwischen dem Problem [**D3DISSUE \_ Begin**](d3dissue-begin.md) und [**D3DISSUE \_ End**](d3dissue-end.md)gezeichnet werden. Dadurch kann eine Anwendung das Okklusions Ergebnis auf 0 überprüfen. NULL ist vollständig verdeckt, d. h., die Pixel sind von der aktuellen Kameraposition aus nicht sichtbar.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE- \_ Zeitstempel**
</dt> <dd>

Gibt einen 64-Bit-Zeitstempel zurück.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ timestampdisjoint**
</dt> <dd>

Verwenden Sie diese Abfrage, um eine Anwendung zu benachrichtigen, wenn sich die Häufigkeit des Zählers für den D3DQUERYTYPE- \_ Zeitstempel geändert hat.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ timestampfreq**
</dt> <dd>

Dieses Abfrageergebnis ist **true** , wenn die Werte von D3DQUERYTYPE \_ timestamp-Abfragen während der gesamten Dauer der D3DQUERYTYPE \_ timestampdisjoint-Abfrage nicht garantiert werden können. Andernfalls ist das Abfrageergebnis **false**.

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ pipelinetimings**
</dt> <dd>

Prozentsatz der Zeit für die Verarbeitung von Pipeline Daten.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ interfacetimings**
</dt> <dd>

Der Prozentsatz der Zeit, die Daten im Treiber verarbeitet.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ vertextimings**
</dt> <dd>

Der Prozentsatz der Zeit, die Vertex-shaderdaten verarbeitet.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ pixeltimings**
</dt> <dd>

Der Prozentsatz der Zeit, die Pixel-shaderdaten verarbeitet.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ bandwidthtimings**
</dt> <dd>

Vergleichsmessungen für den Durchsatz, um die Leistung einer Anwendung besser zu verstehen.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ cacheutilization**
</dt> <dd>

Messen Sie die Leistung der Cache-Treffer Rate für Texturen und indizierte Vertices.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ memorypressure**
</dt> <dd>

Effizienz der Arbeitsspeicher Belegung, die in einer [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) -Struktur enthalten ist.



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DQUERYTYPE \_ memorypressure ist nur in Direct3D9Ex verfügbar, die unter Windows 7 (oder einem höheren aktuellen Betriebssystem) ausgeführt werden.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: kreatequery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
