---
title: VoiceCaption-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die VoiceCaption-Eigenschaft des Commands-Objekts, das den Text zurückgibt oder festlegt, der für das Commands-Objekt im Fenster "Sprachbefehle" angezeigt wird.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b753a1f76769a6d6ec28de3161d01a097108c0c3f973f78e397f1c764fba8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358730"
---
# <a name="voicecaption-property-commands-object"></a>VoiceCaption-Eigenschaft (Commands-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der für das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Sprachbefehlsfenster angezeigt wird, oder legt den Text fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.VoiceCaption-Zeichenfolge_ *  \[  =  \]



| Teil     | BESCHREIBUNG                                               |
|----------|-----------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den angezeigten Text ergibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie die [**Voice-Eigenschaft**](voice-property.md) Ihrer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) festlegen, legen Sie in der Regel auch die **VoiceCaption-Eigenschaft** fest. Die **Texteinstellung VoiceCaption** wird im Fenster "Sprachbefehle" angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) der **Commands-Sammlung** den angezeigten Text. Wenn weder die **VoiceCaption-** noch die **Caption-Eigenschaft** festgelegt ist, werden Befehle in der Sammlung im Fenster "Sprachbefehle" unter "(undefined command)" angezeigt, wenn Ihre Clientanwendung eingabeaktiv wird.

Die **Einstellung VoiceCaption** bestimmt auch den Text, der im Lauschenden Tipp angezeigt wird, um die Befehle anzugeben, für die das Zeichen lauscht.

## <a name="see-also"></a>Weitere Informationen

[Caption-Eigenschaft](caption-property.md)


 

 
