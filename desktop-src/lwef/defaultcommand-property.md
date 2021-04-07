---
title: DefaultCommand (Eigenschaft)
description: DefaultCommand (Eigenschaft)
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038915"
---
# <a name="defaultcommand-property"></a>DefaultCommand (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Standardbefehl für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt zurück oder legt ihn fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. * * * Zeichen* *  **("***Merkmal-ID***"). Commands. DefaultCommand** - \[  =  *Zeichenfolge*\]



| Teil     | BESCHREIBUNG                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Ein Zeichen folgen Wert, der den Namen (ID) des [**Befehls**](/windows/desktop/lwef/the-command-object)identifiziert. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ermöglicht es Ihnen, einen [**Befehl**](/windows/desktop/lwef/the-command-object) in der [**Befehls Auflistung**](/windows/desktop/lwef/the-commands-collection-object) als Standardbefehl festzulegen, wodurch er fett formatiert wird. Dies ändert nicht die Befehls Behandlung oder Doppelklick Ereignisse.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

 

 