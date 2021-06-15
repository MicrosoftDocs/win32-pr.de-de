---
title: FontName-Eigenschaft (Balloon-Objekt)
description: Erfahren Sie mehr über die FontName Balloon-Objekteigenschaft. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068266"
---
# <a name="fontname-property-balloon-object"></a>FontName-Eigenschaft (Balloon-Objekt)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Schriftart zurück, die im Wort balloon für das angegebene Zeichen verwendet wird, oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Balloon.FontName-Schriftart_ *  \[  =  \]



| Teil   | Beschreibung                                      |
|--------|--------------------------------------------------|
| *Schriftart* | Ein Zeichenfolgenwert, der dem Namen der Schriftart entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**FontName-Eigenschaft**](fontname-property.md) definiert die Schriftart, die zum Anzeigen von Text im Wortsprechblasenfenster einer Zeichenfolge verwendet wird. Der Standardwert für die Schriftarteinstellungen der Wortsprechblase eines Zeichens wird im Microsoft Agent-Zeichen-Editor festgelegt. Darüber hinaus kann der Benutzer Schriftarteinstellungen für alle Zeichen im Microsoft Agent-Eigenschaftenblatt überschreiben.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die [**Eigenschaften FontName**](fontname-property.md) und [**FontCharSet**](fontcharset-property.md) für das Zeichen, um zu bestimmen, ob sie für Ihr Locale geeignet sind. Möglicherweise müssen Sie diese Werte festlegen, bevor Sie die [**Speak-Methode**](speak-method.md) verwenden, um eine geeignete Textanzeige im Wortsprechblasen zu gewährleisten.

 

 

 




