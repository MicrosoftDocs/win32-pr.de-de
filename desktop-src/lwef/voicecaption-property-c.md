---
title: VoiceCaption-Eigenschaft (Befehlsobjekt)
description: Erfahren Sie mehr über die VoiceCaption-Eigenschaft des Command-Objekts, mit der der für das Command-Objekt im Fenster "Sprachbefehle" angezeigte Text bestimmt oder zurückgegeben wird.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1e911a4351483aeeea9258679d4321110b49c3d0c51fc49282701b027d27e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665050"
---
# <a name="voicecaption-property-command-object"></a>VoiceCaption-Eigenschaft (Befehlsobjekt)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt den Text fest, der für das Command-Objekt im Fenster für [**Sprachbefehle**](/windows/desktop/lwef/the-command-object) angezeigt wird, oder gibt diesen zurück.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Befehle("_*_Name_*_"). VoiceCaption-Zeichenfolge_ *  \[  =  \]



| Teil     | Beschreibung                                               |
|----------|-----------------------------------------------------------|
| *string* | Ein Zeichenfolgenausdruck, der den angezeigten Text auswertet. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Sammlung**](https://www.bing.com/search?q=**Commands**) definieren und dessen [**Voice-Eigenschaft**](voice-property.md) festlegen, legen Sie in der Regel auch die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) fest. Dieser Text wird im Fenster Sprachbefehle angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) den angezeigten Text. Wenn weder **die VoiceCaption-** noch **die Caption-Eigenschaft** festgelegt ist, wird der Befehl nicht im Fenster Sprachbefehle angezeigt.

### <a name="see-also"></a>Weitere Informationen

[**Caption-Eigenschaft**](caption-property.md)


 

 
