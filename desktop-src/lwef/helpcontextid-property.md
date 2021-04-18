---
title: HelpContextID-Eigenschaft (Commands-Auflistungs Objekt)
description: HelpContextID (Eigenschaft)
ms.assetid: 8b8ac1c6-1a34-45f1-a0a6-2ae14ad6adef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d530a1563080108ef2a2798589519ecca03416
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474922"
---
# <a name="helpcontextid-property-commands-collection-object"></a>HelpContextID-Eigenschaft (Commands-Auflistungs Objekt)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt eine zugeordnete Kontext Nummer für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt zurück oder legt diese fest. Wird verwendet, um kontextbezogene Hilfe für das **Commands** -Objekt bereitzustellen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Befehle ("_*_Name_*_"). HelpContextID_- *  \[  =  *Nummer*\]



| Teil     | BESCHREIBUNG                                   |
|----------|-----------------------------------------------|
| *Number* | Eine ganze Zahl, die eine gültige Kontext Nummer angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Objekt auswählt. Wenn Sie in **HelpContextID** eine Kontext Nummer festlegen, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch diese Kontext Nummer identifiziert wird.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**HelpFile (Eigenschaft)**](helpfile-property.md)


 

 
