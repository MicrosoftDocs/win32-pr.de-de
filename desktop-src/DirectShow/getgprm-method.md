---
description: Die getgprm-Methode ruft das angegebene allgemeine Parameter Register ab.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Getgprm-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522312"
---
# <a name="getgprm-method"></a>Getgprm-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetGPRM` Methode ruft das angegebene allgemeine Parameter Register ab.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Gibt das Register an, das als ganze Zahl abgerufen wird. Der Wert muss zwischen 0 und 15 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der das angegebene Register darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist für DVD-Navigations-oder Wiedergabe Funktionen mit dem **mswebdvd** -Objekt nicht erforderlich. Sie wird für diejenigen bereitgestellt, die über ein umfassendes Verständnis der DVD-Spezifikation verfügen, die erweiterte Funktionen implementieren möchte. Gprms können verwendet werden, um beliebige Werte zu speichern, sodass Sie frei festgelegt und gelesen werden können. Da jedoch gprms auch zum Speichern von Disk-Befehlen verwendet werden, kann das Ändern ihrer Werte mithilfe von [**setgprm**](setgprm-method.md) zu unvorhersehbarem Verhalten führen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Setgprm**](setgprm-method.md)
</dt> </dl>

 

 



