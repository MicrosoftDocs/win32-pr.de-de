---
title: Voicecaption-Eigenschaft (Commands-Objekt)
description: Voicecaption (Eigenschaft)
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739480"
---
# <a name="voicecaption-property-commands-object"></a>Voicecaption-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt im Fenster Sprachbefehle angezeigt wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Commands. voicecaption_- *  \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                               |
|----------|-----------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck, der den angezeigten Text ergibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die [**Voice**](voice-property.md) -Eigenschaft der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festlegen, legen Sie in der Regel auch die **voicecaption** -Eigenschaft fest. Die Texteinstellung **voicecaption** wird im Fenster Sprachbefehle angezeigt, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft der **Befehls** Sammlung den angezeigten Text. Wenn weder die **voicecaption** -Eigenschaft noch die **Caption** -Eigenschaft festgelegt ist, werden die Befehle in der Auflistung im Fenster "Sprachbefehle" unter "(nicht definierter Befehl)" angezeigt, wenn die Client Anwendung als Eingabe aktiv wird.

Mit der **voicecaption** -Einstellung wird auch der im Überwachungsport angezeigte Text bestimmt, um die Befehle anzugeben, für die das Zeichen lauscht.

## <a name="see-also"></a>Weitere Informationen

[Caption-Eigenschaft](caption-property.md)


 

 
