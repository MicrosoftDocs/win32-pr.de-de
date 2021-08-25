---
description: Die GetGPRM-Methode ruft das angegebene allgemeine Parameterregister ab.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: GetGPRM-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c46307f1cbec49b4916cdbd528c2b22cfb42bf89a06285c5c779339786599d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812560"
---
# <a name="getgprm-method"></a>GetGPRM-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetGPRM` -Methode ruft das angegebene allgemeine Parameterregister ab.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Gibt das Register an, das als ganze Zahl abgerufen werden soll. Der Wert muss zwischen 0 und 15 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der das angegebene Register darstellt.

## <a name="remarks"></a>Hinweise

Diese Methode ist für dvd-Navigations- oder Wiedergabefunktionen mit dem **MSWebDVD-Objekt** nicht erforderlich. Sie wird für Personen bereitgestellt, die über umfassende Kenntnisse der DVD-Spezifikationen mit erweiterten Features informiert sind. GPRMs können verwendet werden, um beliebige Werte zu speichern, sodass sie frei festgelegt und gelesen werden können. Da GPRMs jedoch auch zum Speichern von Datenträgerbefehlen verwendet werden, kann das Ändern ihrer Werte mithilfe von [**SetGPRM**](setgprm-method.md) zu unvorhersehbarem Verhalten führen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



