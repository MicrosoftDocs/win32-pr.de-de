---
title: Voicecaption-Eigenschaft (Befehls Objekt)
description: Voicecaption (Eigenschaft)
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340299"
---
# <a name="voicecaption-property-command-object"></a>Voicecaption-Eigenschaft (Befehls Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Legt den Text fest, der für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt im Fenster "Sprachbefehle" angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_*_"). Voicecaption_- *  \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                               |
|----------|-----------------------------------------------------------|
| *string* | Ein Zeichen folgen Ausdruck, der den angezeigten Text ergibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt in einer [**Commands**](https://www.bing.com/search?q=**Commands**) -Auflistung definieren und seine [**Voice**](voice-property.md) -Eigenschaft festlegen, legen Sie in der Regel auch seine [**voicecaption**](voicecaption-property.md) -Eigenschaft fest. Dieser Text wird im Fenster "Sprachbefehle" angezeigt, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die-Einstellung für die [**Caption**](caption-property.md) -Eigenschaft den angezeigten Text. Wenn weder die **voicecaption** -noch die **Caption** -Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.

### <a name="see-also"></a>Weitere Informationen

[**Caption-Eigenschaft**](caption-property.md)


 

 
