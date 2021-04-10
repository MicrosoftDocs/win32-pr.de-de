---
title: Muveto-Methode
description: Muveto-Methode
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038991"
---
# <a name="moveto-method"></a>Muveto-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Verschiebt das angegebene Zeichen an den angegebenen Speicherort.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Muveto* *  *x, y*- \[ *Geschwindigkeit*\]



| Teil    | BESCHREIBUNG                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y*   | Erforderlich. Ein *ganzzahliger* Wert, der den linken Rand (*x*) und den oberen Rand (y) des Animations Rahmens angibt. Ausgedrückt diese Koordinaten in Pixel.                                                   |
| *Geschwindigkeit* | Dies ist optional. Ein Long Integer-Wert, der in Millisekunden angibt, wie schnell der Rahmen des Zeichens bewegt wird. Der Standardwert lautet „1000“. Durch die Angabe von NULL (0) wird der Frame verschoben, ohne eine Animation zu spielen. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Server spielt automatisch die entsprechende Animation, die den **Verschiebungs Zuständen zugewiesen** ist. Die Position eines Zeichens basiert auf der linken oberen Ecke des Rahmens.

Wenn Sie eine Objekt Variable deklarieren und diese Methode auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Wenn die zugeordnete Animation nicht auf dem lokalen Computer geladen wurde, legt der Server außerdem die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest. Wenn Sie also das HTTP-Protokoll **für den Zugriff** auf Zeichen-oder Animationsdaten verwenden, verwenden Sie die [**Get**](get-method.md) -Methode, um die Verschiebungs Zustands Animationen vor dem Aufrufen der Methode " **muveto** " zu laden.

Auch wenn die Animation nicht geladen ist, verschiebt der Server den Frame noch immer.

> [!Note]  
> Wenn Sie vor dem Anzeigen des Zeichens " **muveto** " mit einem Wert ungleich 0 (null) aufruft, wird ein Fehlerstatus zurückgegeben, wenn Sie ihm ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zugewiesen haben, da der Wert ungleich 0 (null) angibt, dass Sie versuchen, eine Animation wiederzugeben, wenn das Zeichen nicht sichtbar ist.

 

> [!Note]  
> Der tatsächliche Effekt des *Geschwindigkeits* Parameters kann je nach Geschwindigkeit des Prozessors des Computers und der Priorität anderer Tasks, die auf dem System ausgeführt werden, variieren.

 

 

 