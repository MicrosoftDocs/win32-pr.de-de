---
title: Remove-Methode
description: Remove-Methode
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3337fb25db49f1d6c8ccd6d94f2817340db226e14718cfa7943940fbfb069b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882781"
---
# <a name="remove-method"></a>Remove-Methode

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Entfernt ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) aus der [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Commands.Remove_ * _Name_



| Teil   | BESCHREIBUNG                                                       |
|--------|-------------------------------------------------------------------|
| *Name* | Erforderlich. Ein Zeichenfolgenwert, der der ID für den Befehl entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) aus der Auflistung entfernt wird, wird es nicht mehr angezeigt, wenn das Popupmenü des Zeichens oder im Befehlsfenster angezeigt wird, wenn Ihre Clientanwendung eingabeaktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**RemoveAll-Methode**](removeall-method.md)


 

 