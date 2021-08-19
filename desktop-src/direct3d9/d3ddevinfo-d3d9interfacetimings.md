---
description: Prozent der Zeit, die Daten im Treiber verarbeitet. Mithilfe dieser Statistiken können Fälle identifiziert werden, in denen der Treiber auf andere Ressourcen wartet.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS -Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d7261096ed373620b8438ccce2d353ccf21f1c236028e8c829951fc64ee3725a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989030"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>D3DDEVINFO \_ D3D9INTERFACETIMINGS-Struktur

Prozent der Zeit, die Daten im Treiber verarbeitet. Mithilfe dieser Statistiken können Fälle identifiziert werden, in denen der Treiber auf andere Ressourcen wartet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>Member

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, die der Treiber auf den Abschluss der GPU mithilfe einer gesperrten Ressource gewartet hat [(D3DLOCK \_ DONOTWAIT](d3dlock.md) wurde nicht angegeben).

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, die der Treiber auf den Abschluss der GPU-Verarbeitung einiger Befehle gewartet hat, bevor der Treiber mehr senden konnte. Dies weist darauf hin, dass dem Treiber der Platz zum Senden von Befehlen an die GPU nicht mehr zur Verfügung steht.

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, die der Treiber auf eine Reduzierung der GPU-Latenz auf weniger als drei Renderingframes gewartet hat.

Wenn eine Anwendung gpu-eingeschränkt ist, muss der Treiber die CPU so lange einstellen, bis die GPU innerhalb von drei Frames ausgeführt wird. Dadurch wird verhindert, dass eine Anwendung Renderingaufrufe in sekundenschnelle in die Warteschlange einschlange, was die Latenz zwischen der Eingabe neuer Daten durch den Benutzer und dem Sehen der Ergebnisse dieser Eingabe erheblich erhöhen kann. Im Allgemeinen kann der Treiber nachverfolgen, wie oft [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufgerufen wird, um zu verhindern, dass mehr als drei Frames von Renderingarbeit in die Warteschlange warteschlangen.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Zeit, die der Treiber auf eine Ressource gewartet hat, für die keine Pipeline ausgeführt werden kann (die parallel betrieben wird). Eine Anwendung sollte aus Leistungsgründen die Verwendung einer Nichtpipelineressource vermeiden.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Wartezeit des Treibers auf andere GPU-Verarbeitung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit diesen Metriken können Sie erkennen, wann ein Treiber wartet und worauf er wartet. Hohe Prozentsätze sind nicht unbedingt ein Problem.

Diese system globalen Metriken können implementiert werden oder nicht. Abhängig von der spezifischen Hardware unterstützen diese Metriken möglicherweise nicht mehrere Abfragen gleichzeitig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
