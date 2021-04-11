---
title: Remove-Methode
description: Remove-Methode
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315135"
---
# <a name="remove-method"></a>Remove-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Entfernt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt aus der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID ***"). Befehle. Remove*** Name*



| Teil   | BESCHREIBUNG                                                       |
|--------|-------------------------------------------------------------------|
| *Name* | Erforderlich. Ein Zeichen folgen Wert, der der ID für den Befehl entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt aus der Auflistung entfernt wird, wird es nicht mehr angezeigt, wenn das Popupmenü des Zeichens angezeigt wird, oder im Befehlsfenster, wenn die Client Anwendung aktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**RemoveAll-Methode**](removeall-method.md)


 

 