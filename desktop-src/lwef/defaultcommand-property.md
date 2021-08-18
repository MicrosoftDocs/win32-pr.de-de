---
title: DefaultCommand-Eigenschaft
description: DefaultCommand-Eigenschaft
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7aec703ffbabb98ae16609b0dcb01767fda5c38b42ed40f204e3a3bae5766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693635"
---
# <a name="defaultcommand-property"></a>DefaultCommand-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Standardbefehl des Commands-Objekts zurück oder [**legt**](/windows/desktop/lwef/the-commands-collection-object) diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.**Characters* *  **("**_CharacterID_*_"). Commands.DefaultCommand-Zeichenfolge_* \[  =  \]



| Teil     | Beschreibung                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | Ein Zeichenfolgenwert, der den Namen (ID) des [**Befehls angibt.**](/windows/desktop/lwef/the-command-object) |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit dieser Eigenschaft können Sie einen Befehl [**in**](/windows/desktop/lwef/the-command-object) ihrer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) als Standardbefehl festlegen und fett formatiert rendern. Dadurch wird die Befehlsbehandlung oder das Doppelklicken auf Ereignisse nicht geändert.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

 

 