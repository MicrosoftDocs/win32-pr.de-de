---
description: Wenn Sie mehrere erkenungen verwenden, können Sie mithilfe der Auflistung Erkennungs Tools verfügbare erkenungen auflisten und einem Benutzer ermöglichen, zwischen diesen zu wählen.
ms.assetid: 1b89def0-3491-42da-9138-5280002e447a
title: Verwenden der Erkennungs Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d38625b3c6d4b8ed2475393ba45ae97b5bdc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344435"
---
# <a name="using-the-recognizers-collection"></a>Verwenden der Erkennungs Sammlung

Wenn Sie mehrere erkenungen verwenden, können Sie mithilfe der Auflistung [**Erkennungs**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) Tools verfügbare erkenungen auflisten und einem Benutzer ermöglichen, zwischen diesen zu wählen. Eine **Erkennungs** Auflistung prüft auf installierte erkenungen, fragt die Attribute der [**Erkennungs**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) Objekte ab und speichert die Ergebnisse. Anwendungen können die Auflistung der **Erkennungs** Programme verwenden, um eine Liste verfügbarer erkenungen anzuzeigen, ohne jede Erkennungs-DLL zu laden.

> [!Note]  
> Die [**Erkennungs**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) Sammlung verwendet die Systemregistrierung, um nach Microsoft-erkenungen und Erkennungs Programmen von Drittanbietern zu suchen.

 

In der folgenden Tabelle sind die Werte der sprach Bezeichner aufgeführt, die von den Microsoft-erkenungen unterstützt werden.

> [!Note]  
> Der Microsoft Gestenerkennung sind keine sprach Bezeichner zugeordnet.

 



| Erkennungs Name                                                      | Primäre Sprach-ID, unter Sprachen-ID (in der Reihenfolge unterstützt)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestenerkennung von Microsoft<br/>                              | Keine<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Handschrifterkennung von Microsoft English (Vereinigtes Königreich)<br/> | LANG \_ Englisch, sublang \_ English \_ UK<br/> LANG \_ Englisch, sublang \_ English \_ Eire<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Handschrifterkennung von Microsoft English (USA)<br/>  | LANG \_ Englisch, sublang \_ Englisch ( \_ USA)<br/> LANG \_ Englisch, sublang \_ English \_ aus<br/> LANG \_ Englisch, sublang \_ English \_ Belize<br/> LANG \_ Englisch, unter lang \_ Englisch \_<br/> LANG \_ Englisch, sublang \_ English \_ Karibik<br/> LANG \_ Englisch, sublang \_ English \_ Jamaika<br/> LANG \_ Englisch, unter lang \_ English \_ NZ<br/> LANG \_ Englisch, unter lang \_ Englisch ( \_ Philippinen)<br/> LANG \_ Englisch, sublang \_ Englisch ( \_ Südafrika \_ )<br/> LANG \_ Englisch, sublang \_ English \_ Trinidad<br/> LANG \_ Englisch, sublang \_ English \_ Simbabwe<br/> LANG \_ Englisch, unter lang \_ neutral<br/> |
| Microsoft französische Handschrifterkennung<br/>                   | LANG \_ Französisch, unter lang \_ Französisch<br/> LANG \_ Französisch, sublang \_ Französisch ( \_ Belgien)<br/> LANG \_ Französisch, unter lang \_ Französisch \_ Kanada<br/> LANG \_ Französisch, sublang \_ Französisch ( \_ Luxemburg)<br/> LANG \_ Französisch, sublang \_ Französisch \_ Monaco<br/> LANG \_ Französisch, unter lang \_ Französisch \_ Schweiz<br/> LANG \_ Französisch, unter lang \_ neutral<br/>                                                                                                                                                                                                                                                                                     |
| Deutsche Handschrifterkennung von Microsoft<br/>                   | LANG \_ Deutsch, sublang \_ Deutsch<br/> LANG \_ Deutsch, unter \_ Deutsch Deutsch (Deutsch) \_<br/> LANG \_ Deutsch, sublang \_ Deutsch ( \_ Liechtenstein)<br/> LANG \_ Deutsch, sublang \_ Deutsch \_ Luxemburg<br/> LANG \_ Deutsch, unter lang \_ Deutsch \_ Schweiz<br/> LANG \_ Deutsch, unter lang \_ neutral<br/>                                                                                                                                                                                                                                                                                                                                |
| Microsoft Spanish-Handschrifterkennung<br/>                  | LANG \_ Spanisch, unter lang \_ Spanisch<br/> LANG \_ Spanisch, unter lang \_ neutral<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Microsoft-Handschrifterkennung<br/>                 | LANG \_ Japanisch, unter lang \_ neutral<br/> LANG \_ Japanisch, sublang \_ Standard<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Microsoft koreanische Handschrifterkennung<br/>                   | LANG \_ Koreanisch, unter lang \_ neutral<br/> LANG \_ Koreanisch, sublang \_ Standard<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Microsoft Chinesisch (vereinfacht) Handschrifterkennung<br/>     | LANG \_ Chinesisch, sublang \_ Chinesisch ( \_ vereinfacht)<br/> LANG \_ Chinesisch, sublang \_ Chinesisch ( \_ Singapur)<br/> LANG \_ Chinesisch, unter lang \_ neutral<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Microsoft Chinesisch (traditionell) Handschrifterkennung<br/>    | LANG \_ Chinesisch, sublang \_ Chinesisch \_ traditionell<br/> LANG \_ Chinesisch, sublang \_ Chinesisch ( \_ Hongkong)<br/> LANG \_ Chinesisch, sublang \_ Chinesisch ( \_ Macau)<br/> LANG \_ Chinesisch, unter lang \_ neutral<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Weitere Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](../intl/language-identifier-constants-and-strings.md)Zeichen folgen.

 

 
