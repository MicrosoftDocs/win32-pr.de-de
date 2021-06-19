---
title: VoiceCaption-Eigenschaft (Commands-Objekt)
description: Erfahren Sie mehr über die VoiceCaption-Eigenschaft des Commands-Objekts, die den für das Commands-Objekt im Fenster "Voice Commands" angezeigten Text zurückgibt oder legt diesen fest.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396125"
---
# <a name="voicecaption-property-commands-object"></a>VoiceCaption-Eigenschaft (Commands-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Text zurück, der für das [**Commands-Objekt**](/windows/desktop/lwef/the-commands-collection-object) im Fenster für Sprachbefehle angezeigt wird, oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.VoiceCaption-Zeichenfolge_ *  \[  =  \]



| Teil     | Beschreibung                                               |
|----------|-----------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den angezeigten Text auswertet. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die [**Voice-Eigenschaft**](voice-property.md) Ihrer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) festlegen, legen Sie in der Regel auch deren **VoiceCaption-Eigenschaft** fest. Die **Texteinstellung VoiceCaption** wird im Fenster Sprachbefehle angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) der **Commands-Auflistung** den angezeigten Text. Wenn weder **die VoiceCaption-** noch die **Caption-Eigenschaft** festgelegt ist, werden Befehle in der Sammlung im Fenster Für Sprachbefehle unter "(nicht definierter Befehl)" angezeigt, wenn Ihre Clientanwendung eingabeaktiv wird.

Die **VoiceCaption-Einstellung** bestimmt auch den im Lauschenden Tipp angezeigten Text, um die Befehle anzugeben, auf die das Zeichen lausiert.

## <a name="see-also"></a>Weitere Informationen

[Caption-Eigenschaft](caption-property.md)


 

 
