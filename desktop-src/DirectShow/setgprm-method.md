---
description: Die setgprm-Methode legt den angegebenen allgemeinen Parameter Register auf den angegebenen Wert fest.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Setgprm-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346811"
---
# <a name="setgprm-method"></a>Setgprm-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SetGPRM` Methode legt den angegebenen allgemeinen Parameter Register auf den angegebenen Wert fest.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Gibt das allgemeine Parameter Register an, das als ganze Zahl festgelegt werden soll. Der ganzzahlige Wert muss zwischen 0 und 15 liegen.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nWert*
</dt> <dd>

Gibt den neuen Wert für das Register als Ganzzahl an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Allgemeine Parameter Register (oder gprms) sind 16-Bit-Register, die von den einzelnen Datenträgern für die temporäre Datenspeicherung auf besondere Weise verwendet werden können. Eine Player Anwendung muss nicht auf diese Register für eine Standard Wiedergabe oder ein Navigations Steuerelement mithilfe des **mswebdvd** -Objekts zugreifen. Diese Methode wird für Player Anwendungen bereitgestellt, die erweiterte Funktionen implementieren. Versuchen Sie nicht, die gprms direkt zu ändern, es sei denn, Sie haben umfassende Kenntnisse über die DVD-Spezifikation und die Art und Weise, in der die gprms auf der zu Wiedergabe enden Festplatte verwendet werden. Wenn Sie diese Werte ändern, kann dies zu unvorhersehbarem Verhalten führen.

 

 



