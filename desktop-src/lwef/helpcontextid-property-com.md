---
title: HelpContextID-Eigenschaft (Befehls Objekt)
description: HelpContextID (Eigenschaft)
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102754"
---
# <a name="helpcontextid-property-command-object"></a>HelpContextID-Eigenschaft (Befehls Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontext Nummer für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zurück oder legt diese fest. Wird verwendet, um kontextbezogene Hilfe für das **Befehls** Objekt bereitzustellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Befehle (""). HelpContextID_- *  \[  =  *Nummer*\]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontext Nummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens auf die Datei festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt. Wenn Sie in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer festlegen, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile (Eigenschaft)**](helpfile-property.md)


 

 
