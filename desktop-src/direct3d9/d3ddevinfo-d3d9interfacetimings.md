---
description: Der Prozentsatz der Zeit, die Daten im Treiber verarbeitet. Mithilfe dieser Statistiken können Fälle identifiziert werden, in denen der Treiber auf andere Ressourcen wartet.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354357"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>D3DDEVINFO \_ D3D9INTERFACETIMINGS-Struktur

Der Prozentsatz der Zeit, die Daten im Treiber verarbeitet. Mithilfe dieser Statistiken können Fälle identifiziert werden, in denen der Treiber auf andere Ressourcen wartet.

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

**Waitingforgputougenapplicationresourcetimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit, die der Treiber auf die Beendigung der GPU mithilfe einer gesperrten Ressource gewartet hat (und [D3DLOCK \_ donotwait](d3dlock.md) nicht angegeben wurde).

</dd> <dt>

**Waitingforgputoakzeptmorecommandstimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit, die der Treiber auf die Verarbeitung einiger Befehle durch die GPU gewartet hat, bevor der Treiber mehr senden konnte. Dies gibt an, dass der Treiber nicht mehr genügend Platz zum Senden von Befehlen an die GPU hat.

</dd> <dt>

**Waitingforgputostaywithinlatencytimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit, die der Treiber gewartet hat, bis die GPU-Latenz auf weniger als drei renderingframes reduziert wurde.

Wenn eine Anwendung GPU-begrenzt ist, muss der Treiber die CPU so lange einstellen, bis die GPU innerhalb von drei Frames erreicht wird. Dadurch wird verhindert, dass eine Anwendung eine große Anzahl von renderingaufrufen in die Warteschlange eingereiht, was die Wartezeit zwischen dem Zeitpunkt, zu dem der Benutzer neue Daten eingibt, und dem Zeitpunkt, zu dem der Benutzer die Ergebnisse dieser Eingabe sieht Im Allgemeinen kann der Treiber überprüfen, wie oft der [**vorhandene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufgerufen wird, um zu verhindern, dass mehr als drei Frames der Rendering-Arbeit in die Warteschlange eingereiht werden.

</dd> <dt>

**Waitingforgpuexclusiveresourcetimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit, die der Treiber auf eine Ressource gewartet hat, die nicht Pipeline (parallel betrieben) werden kann. Eine Anwendung kann aus Leistungsgründen die Verwendung einer Ressource ohne Pipelines vermeiden.

</dd> <dt>

**Waitingforgpuothertimeprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Prozentsatz der Zeit, die der Treiber auf die Verarbeitung anderer GPU gewartet hat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Metriken helfen, zu bestimmen, wann ein Treiber wartet und worauf er wartet. Hohe Prozentsätze sind nicht notwendigerweise ein Problem.

Diese systemweiten Metriken können oder nicht implementiert werden. Abhängig von der jeweiligen Hardware unterstützen diese Metriken möglicherweise nicht mehrere Abfragen gleichzeitig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
