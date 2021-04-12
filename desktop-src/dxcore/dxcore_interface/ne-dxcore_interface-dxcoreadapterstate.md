---
title: DXCoreAdapterState
description: Definiert Konstanten, die Arten von DXCore-Adapter Zuständen angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315560"
---
# <a name="dxcoreadapterstate-enum"></a>Dxcoreadapterstate-Aufzählung

Definiert Konstanten, die Arten von DXCore-Adapter Zuständen angeben. Übergeben Sie eine dieser Konstanten an die [idxcoreadapter:: querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md) -Methode, um das Adapter Zustands Element für eine Statusart abzurufen. übergeben Sie eine Konstante an die [idxcoreadapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) -Methode, um die Informationen eines Adapters für ein Zustands Element festzulegen.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Konstanten

### <a name="isdriverupdateinprogress"></a>Isdriverupdaterprogress

Gibt den <em>isdriverupdateinprogress</em> -Adapter Status an, der `true` angibt, dass ein Treiberupdate auf dem Adapter initiiert, aber noch nicht abgeschlossen wurde. Wenn das Treiberupdate bereits abgeschlossen wurde, wird der Adapter ungültig, und der [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md) -Rückruf gibt ein <b>HRESULT</b> <b>DXGI_ERROR_DEVICE_REMOVED</b>zurück.

Beim Aufrufen von [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat das <em>isdriverupdateinprogress</em> -Zustands Element den Typ <b>uint8_t</b>, der einen booleschen Wert darstellt.

<b>Wichtig</b>. Dieses Zustands Element wird für [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)nicht unterstützt.

### <a name="adaptermemorybudget"></a>Adaptermemorybudget

Gibt den <em>adaptermemorybudget</em> -Adapter Status an, der das Arbeitsspeicher Budget des Adapters für den Adapter abruft oder anfordert.

Beim Aufrufen von [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat <em>der adaptermemorybudget</em> -Adapter Status den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">dxcoreadaptermemorybudgetnodesegmentgroup</a> für *inputstatedetails* und den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">dxcoreadaptermemorybudget</a> für *OUTPUTBUFFER*.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter:: querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md), [idxcoreadapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)