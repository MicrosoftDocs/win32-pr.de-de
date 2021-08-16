---
title: FontCharSet-Eigenschaft
description: FontCharSet-Eigenschaft
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca702bb1ff9dfe020f7fdb43b57a74fd1e5e46a14caff8735f21170ed8e2f1b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479328"
---
# <a name="fontcharset-property"></a>FontCharSet-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Zeichensatz für die Schriftart zurück, die im Wortsprechblasen des angegebenen Zeichens angezeigt wird, oder legt den Zeichensatz fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Balloon.FontCharSet-Wert_ *  \[  =  \]



| Teil    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Ein ganzzahliger Wert, der den von der Schriftart verwendeten Zeichensatz angibt. Im Folgenden finden Sie einige allgemeine Einstellungen für value: 0 Standard Windows Characters (ANSI).<br/> 1 Standardzeichensatz.<br/> 2 Der Symbolzeichensatz.<br/> 128 Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), eindeutig für die japanische Version Windows.<br/> 129 Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), eindeutig für die koreanische Version Windows.<br/> 134 Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), eindeutig für die vereinfachte chinesische Version Windows.<br/> 136 Doppel-Byte-Zeichensatz (Double-Byte Character Set, DBCS), eindeutig für die traditionelle chinesische Version Windows.<br/> 255 erweiterte Zeichen, die normalerweise von Microsoft MS-DOS-Anwendungen angezeigt werden.<br/> Weitere Zeichensatzwerte finden Sie in der Dokumentation zum Platform SDK.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Standardwert für den Zeichensatz der Wortsprechblase eines Zeichens wird im Microsoft Agent-Zeichen-Editor festgelegt. Darüber hinaus kann der Benutzer die Zeichensatzeinstellungen für alle Zeichen im Microsoft Agent-Eigenschaftenblatt überschreiben.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die [**Eigenschaften FontName**](fontname-property.md) und **FontCharSet** für das Zeichen, um zu ermitteln, ob sie für Ihr Locale geeignet sind. Möglicherweise müssen Sie diese Werte festlegen, bevor Sie die [**Speak-Methode**](speak-method.md) verwenden, um eine geeignete Textanzeige im Wortsprechblasen zu gewährleisten.

 

## <a name="see-also"></a>Weitere Informationen

[**FontName-Eigenschaft**](fontname-property.md)


 

 





