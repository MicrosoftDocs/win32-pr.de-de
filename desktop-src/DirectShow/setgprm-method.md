---
description: Die SetGPRM-Methode legt das angegebene allgemeine Parameterregister auf den angegebenen Wert fest.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: SetGPRM-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c217f0235ca5b055e20102f553e9e23f5b93e6dd9c3d74db560584690a669ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078860"
---
# <a name="setgprm-method"></a>SetGPRM-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SetGPRM` -Methode legt das angegebene allgemeine Parameterregister auf den angegebenen Wert fest.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Gibt das allgemeine Parameterregister an, das als ganze Zahl festgelegt werden soll. Der Ganzzahlwert muss zwischen 0 und 15 liegen.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*
</dt> <dd>

Gibt den neuen Wert für das Register als ganze Zahl an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Allgemeine Parameterregister oder GPRMs sind 16-Bit-Register, die jeder Datenträger auf einzigartige Weise für die temporäre Datenspeicherung verwenden kann. Eine Playeranwendung muss mithilfe des **MSWebDVD-Objekts** nicht auf diese Register für ein Standardwiedergabe- oder Navigationssteuerfeld zugreifen. Diese Methode wird für Playeranwendungen bereitgestellt, die erweiterte Funktionen implementieren. Versuchen Sie nicht, die GPRMs direkt zu ändern, es sei denn, Sie verfügen über umfassende Kenntnisse der DVD-Spezifikation und der Art und Weise, wie die GPRMs auf dem jeweiligen Datenträger verwendet werden, um abgespielt zu werden. Das Ändern dieser Werte kann zu unvorhersehbarem Verhalten führen.

 

 



