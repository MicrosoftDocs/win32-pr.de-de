---
title: Fontcharset (Eigenschaft)
description: Fontcharset (Eigenschaft)
ms.assetid: 2f23a242-d620-4766-8f59-cf158aa55969
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4561de9af823b4213266a93b7bfa2e29588c3c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311016"
---
# <a name="fontcharset-property"></a>Fontcharset (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Zeichensatz für die in der Wort Sprechblase des angegebenen Zeichens angezeigte Schriftart zurück oder legt diesen fest.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Balloon. fontcharset*- *  \[  =  *Wert*\]



| Teil    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *value* | Ein ganzzahliger Wert, der den von der Schriftart verwendeten Zeichensatz angibt. Im folgenden finden Sie einige allgemeine Einstellungen für Wert: 0 Standard mäßige Windows-Zeichen (ANSI).<br/> 1 Standardzeichensatz.<br/> 2 der Symbol Zeichensatz.<br/> 128 Doppelbyte-Zeichensatz (DBCS), der für die japanische Version von Windows eindeutig ist.<br/> 129 Doppelbyte-Zeichensatz (DBCS), der für die koreanische Version von Windows eindeutig ist.<br/> 134 Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS), der für die vereinfachte chinesische Version von Windows eindeutig ist<br/> 136 Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS), der für die traditionelle chinesische Version von Windows eindeutig ist<br/> 255 erweiterte Zeichen, die normalerweise von Microsoft MS-DOS-Anwendungen angezeigt werden.<br/> Weitere Zeichensatz Werte finden Sie in der Platform SDK-Dokumentation.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Standardwert für den Zeichensatz der Wort Sprechblase eines Zeichens wird im Microsoft-Agent-Zeichen-Editor festgelegt. Außerdem kann der Benutzer die Zeichensatz Einstellungen für alle Zeichen im Microsoft-Agent-Eigenschaften Blatt überschreiben.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Wenn Sie ein Zeichen verwenden, das Sie nicht kompiliert haben, überprüfen Sie die Eigenschaften [**FontName**](fontname-property.md) und **fontcharset** auf das Zeichen, um zu bestimmen, ob Sie für Ihr Gebiets Schema geeignet sind. Sie müssen diese Werte möglicherweise vor der Verwendung der [**Sprech**](speak-method.md) Methode festlegen, um die entsprechende Textanzeige innerhalb der Word-Sprechblase sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**FontName-Eigenschaft**](fontname-property.md)


 

 





