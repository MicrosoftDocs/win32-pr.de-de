---
title: VoiceCaption-Eigenschaft (Command-Objekt)
description: Erfahren Sie mehr über die VoiceCaption-Eigenschaft des Command-Objekts, das den Text festlegt oder zurückgibt, der für das Command-Objekt im Fenster "Sprachbefehle" angezeigt wird.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396165"
---
# <a name="voicecaption-property-command-object"></a>VoiceCaption-Eigenschaft (Command-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt den Text fest, der für das [**Command-Objekt**](/windows/desktop/lwef/the-command-object) im Fenster "Sprachbefehle" angezeigt wird, oder gibt den Text zurück.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). VoiceCaption-Zeichenfolge_ *  \[  =  \]



| Teil     | Beschreibung                                               |
|----------|-----------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den angezeigten Text ergibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Sammlung**](https://www.bing.com/search?q=**Commands**) definieren und dessen [**Voice-Eigenschaft**](voice-property.md) festlegen, legen Sie in der Regel auch die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) fest. Dieser Text wird im Sprachbefehlsfenster angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) den angezeigten Text. Wenn weder die **VoiceCaption-** noch **die Caption-Eigenschaft** festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.

### <a name="see-also"></a>Weitere Informationen

[**Caption-Eigenschaft**](caption-property.md)


 

 
