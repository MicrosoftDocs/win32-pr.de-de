---
title: FontName-Eigenschaft (Sprechblasen Objekt)
description: FontName-Eigenschaft
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102734"
---
# <a name="fontname-property-balloon-object"></a>FontName-Eigenschaft (Sprechblasen Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die in der Wort Sprechblase für das angegebene Zeichen verwendete Schriftart zurück oder legt diese fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Sprechblase. FontName_( *  \[  =  *Schriftart* )\]



| Teil   | BESCHREIBUNG                                      |
|--------|--------------------------------------------------|
| *Raster* | Ein Zeichen folgen Wert, der dem Namen der Schriftart entspricht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**FontName**](fontname-property.md) -Eigenschaft definiert die Schriftart, die zum Anzeigen von Text im Word-sprecherfenster einer Zeichenfolge verwendet wird. Der Standardwert für die Schriftart Einstellungen der Word-Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor festgelegt. Außerdem kann der Benutzer die Schriftart Einstellungen für alle Zeichen auf dem Eigenschaften Blatt Microsoft-Agent überschreiben.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die Eigenschaften [**FontName**](fontname-property.md) und [**fontcharset**](fontcharset-property.md) auf das Zeichen, um zu bestimmen, ob Sie für Ihr Gebiets Schema geeignet sind. Sie müssen diese Werte möglicherweise vor der Verwendung der [**Sprech**](speak-method.md) Methode festlegen, um die entsprechende Textanzeige innerhalb der Word-Sprechblase sicherzustellen.

 

 

 




