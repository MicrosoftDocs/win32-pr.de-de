---
title: HelpFile (Eigenschaft)
description: HelpFile (Eigenschaft)
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710920"
---
# <a name="helpfile-property"></a>HelpFile (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Pfad und den Dateinamen für eine kontextabhängige Microsoft Windows-Hilfedatei zurück, die von der Client Anwendung bereitgestellt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. ***Zeichen ("*** Merkmal-ID * * *"). HelpFile* *  \[  =  *Dateiname*\]



| Teil       | BESCHREIBUNG                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Filename* | Ein Zeichen folgen Ausdruck, der den Pfad und den Dateinamen der Windows-Hilfedatei angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die **HelpFile** -Eigenschaft des Zeichens festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmadeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer auf das Zeichen klickt oder einen Befehl aus dem Popupmenü auswählt. Wenn Sie in der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft des ausgewählten Befehls eine Kontext Nummer angegeben haben, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Helpmudeon-Eigenschaft**](helpmodeon-property.md), [ **HelpContextID-Eigenschaft**](helpcontextid-property.md)


 

 




