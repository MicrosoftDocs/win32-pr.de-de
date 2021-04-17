---
title: DXCoreAdapterMemoryBudget
description: Beschreibt das Arbeitsspeicher Budget für einen Adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474069"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>Dxcoreadaptermemorybudget-Struktur

Gibt den <em>adaptermemorybudget</em> -Adapter Status an, der das Arbeitsspeicher Budget des Adapters für den Adapter abruft oder anfordert. Das festlegen (anfordern) eines Budgets gibt den mindestens erforderlichen physischen Speicher an, der in Byte für den Adapter reserviert werden soll. Es wird empfohlen, dass Sie eine Adapter Reservierung festlegen, um die Menge an physischem Arbeitsspeicher anzugeben, die Ihre Anwendung nicht unterlassen kann. Dieser Wert hilft dem Betriebssystem, die Auswirkungen von großen Speicherdruck Situationen schnell zu minimieren.

Beim Aufrufen von [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat <em>der adaptermemorybudget</em> -Adapter Status den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">dxcoreadaptermemorybudgetnodesegmentgroup</a> für *inputstatedetails* und den Typ **dxcoreadaptermemorybudget** für *OUTPUTBUFFER*.

Beim Aufrufen [von SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)hat der <em>adaptermemorybudget</em> -Adapter Status den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">dxcoreadaptermemorybudgetnodesegmentgroup</a> für *inputstatedetails*, und geben Sie **uint64_t** für *inputData* ein.

## <a name="syntax"></a>Syntax

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>Member

### <a name="budget"></a>budget

Typ: **uint64_t**

Gibt das vom Betriebssystem bereitgestellte Arbeitsspeicher Budget (in Byte) an, das Ihre Anwendung als Ziel hat. Wenn *CurrentUsage* größer als das *Budget* ist, kann die Anwendung aufgrund der Hintergrund Aktivität durch das Betriebssystem zu einer ungenügenden oder Leistungseinbußen kommen, die anderen Anwendungen eine faire Verwendung des Adapter Speichers bereitstellen soll.

### <a name="currentusage"></a>CurrentUsage

Typ: **uint64_t**

Gibt die Speicherauslastung des aktuellen Adapters für den Anwendungs Speicher in Bytes an.

### <a name="availableforreservation"></a>availableforreservierung

Typ: **uint64_t**

Gibt die Größe des Adapter Speichers in Bytes an, der von der Anwendung für die Reservierung zur Verfügung gestellt wurde. Um diesen Adapter Speicher zu reservieren, sollte Ihre Anwendung [idxcoreadapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) aufrufen, wobei *State* auf [dxcoreadapterstate:: adaptermemorybudget](./ne-dxcore_interface-dxcoreadapterstate.md)festgelegt ist.

### <a name="currentreservation"></a>currentreservation

Typ: **uint64_t**

Gibt die Größe des Adapter Speichers in Bytes an, der für Ihre Anwendung reserviert ist. Das Betriebssystem verwendet die Reservierung als Hinweis, um den minimalen Arbeits Satz Ihrer Anwendung zu bestimmen. Die Anwendung sollte sicherstellen, dass die Speicherauslastung des Adapters zum erfüllen dieser Anforderung verkürzt werden kann.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)