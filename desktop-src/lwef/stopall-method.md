---
title: StopAll-Methode
description: StopAll-Methode
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337642"
---
# <a name="stopall-method"></a>StopAll-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Beendet alle Animations Anforderungen oder angegebenen Anforderungs Typen für das angegebene Zeichen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). StopAll*- *  \[ *Typ*\]



| Teil   | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type* | Dies ist optional. Wenn Sie diesen Parameter verwenden möchten, können Sie einen der folgenden Werte verwenden. Sie können auch mehrere Typen angeben, indem Sie Sie durch Kommas trennen. <br/> "**Get**" <br/> , Um alle [**Get**](get-method.md) -Anforderungen in der Warteschlange anzuhalten.<br/> "**Nonqueuedget**" <br/> Zum Abbrechen aller nicht in die Warteschlange eingereihten [**Get**](get-method.md) -Anforderungen (**Get** -Methode mit **Queue** -Parameter ist auf **false** festgelegt).<br/> "**Verschieben**" <br/> , Um alle in der Warteschlange [**befindlichen Anforderungen für**](moveto-method.md) das Anforderungs Wort anzuhalten<br/> "**Play**" <br/> , Um alle [**Wiedergabe**](play-method.md) Anforderungen in der Warteschlange anzuhalten.<br/> "**Sprechen**" <br/> , Um alle [**sprach**](speak-method.md) Anforderungen in der Warteschlange zu verhindern.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den **Typparameter** nicht festlegen, hält der Server alle Animationen für das Zeichen an, einschließlich Warteschlangen und nicht in die Warteschlange eingereihte [**Get**](get-method.md) -Anforderungen, und löscht seine Animations Warteschlange. Außerdem wird die Wiedergabe eines Zeichens zum Ausblenden oder Einblenden der Animation angehalten.

Diese Methode generiert kein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt.

## <a name="see-also"></a>Weitere Informationen

[**Stop-Methode**](stop-method.md)


 

