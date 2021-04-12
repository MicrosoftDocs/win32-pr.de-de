---
title: Gestureat-Methode
description: Gestureat-Methode
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472804"
---
# <a name="gestureat-method"></a>Gestureat-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die gesturdende Animation für das angegebene Zeichen an der angegebenen Position wieder.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Gestureat* *  *x, y*



| Teil  | BESCHREIBUNG                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y* | Erforderlich. Ein ganzzahliger Wert, der die horizontale Bildschirm Koordinate (*x*) und die vertikale Bildschirm Koordinate (*y*) angibt, auf die das Zeichen zeigt. Diese Koordinaten müssen in Pixel angegeben werden. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Server übernimmt automatisch die entsprechende Animation, um an den angegebenen Speicherort zu Gesten. Die Koordinaten sind immer relativ zum Bildschirm Ursprung (oben links).

Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Wenn die zugeordnete Animation nicht auf dem lokalen Computer geladen wurde, legt der Server außerdem die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlernummer fest. Wenn Sie also das HTTP-Protokoll für den Zugriff auf Daten der Zeichen Animation verwenden, verwenden Sie die [**Get**](get-method.md) -Methode, um die **gestischen** Zustands Animationen zu laden, bevor Sie die **gestureat** -Methode aufrufen.

 

 