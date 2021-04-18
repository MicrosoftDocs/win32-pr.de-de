---
title: HelpContextID-Eigenschaft (Character-Objekt)
description: HelpContextID (Eigenschaft)
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391396"
---
# <a name="helpcontextid-property-characters-object"></a>HelpContextID-Eigenschaft (Character-Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontext Nummer für das Zeichen zurück oder legt diese fest. Wird verwendet, um die kontextbezogene Hilfe für das Zeichen bereitzustellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). HelpContextID_- *  \[  =  *Nummer*\]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontext Nummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um die kontextabhängige Hilfe für das Zeichen zu unterstützen, weisen Sie die Kontext Nummer dem Zeichen zu, das Sie für das zugehörige Hilfethema verwenden, wenn Sie die Hilfedatei kompilieren. Diese Eigenschaft gilt nur für den Client des Zeichens; die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen des Clients aus.

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer auf das Zeichen klickt. Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das Zeichen.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile (Eigenschaft)**](helpfile-property.md)


 

 




