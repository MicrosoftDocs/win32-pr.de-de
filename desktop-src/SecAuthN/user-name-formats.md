---
description: Wenn eine Anwendung die Anmeldeinformationen Verwaltungs-API anmeldeinformationen ein, wird erwartet, dass der Benutzer Informationen einzugeben, die überprüft werden können, entweder vom Betriebssystem oder von der Anwendung.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Benutzernamenformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c2d4a31904e1cdc6c08da596e2db24054389387ef90142001e7f0e6e520567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915545"
---
# <a name="user-name-formats"></a>Benutzernamenformate

Wenn eine Anwendung die Anmeldeinformationen Verwaltungs-API anmeldeinformationen ein, wird erwartet, dass der Benutzer Informationen einzugeben, die überprüft werden können, entweder vom Betriebssystem oder von der Anwendung. Der Benutzer kann Domänenanmeldeinformationen in einem der folgenden Formate angeben:

-   [Benutzerprinzipalname](#user-principal-name)
-   [Downlevel-Anmeldename](#down-level-logon-name)

## <a name="user-principal-name"></a>Benutzerprinzipalname

Das UPN-Format (User [*Principal Name)*](../secgloss/u-gly.md) wird verwendet, um einen Namen im Internetformat anzugeben, z. <b>UserName@Example.Microsoft.com</b> B. . In der folgenden Tabelle sind die Teile eines UPN zusammengefasst.



| Teil                                                        | Beispiel                                |
|-------------------------------------------------------------|----------------------------------------|
| Benutzername. Wird auch als Anmeldename bezeichnet.<br/> | *UserName*<br/>                  |
| Trennzeichen. Ein Zeichenliteral, das At-Zeichen (@).<br/> | @<br/>                           |
| UPN-Suffix. Wird auch als Domänenname bezeichnet.<br/>       | *Example.Microsoft.com* <br/> |



 

Ein UPN kann implizit oder explizit definiert werden. Ein impliziter UPN hat das Formular <b>UserName@DNSDomainName.com</b> . Ein impliziter UPN ist immer dem Konto des Benutzers zugeordnet, auch wenn kein expliziter UPN definiert ist. Ein expliziter UPN hat die Form , wobei sowohl der Name als auch die Suffixzeichenfolge <i><b>Name@Suffix</b></i> explizit vom Administrator definiert werden.

## <a name="down-level-logon-name"></a>Down-Level Anmeldename

Das formatierte Anmeldenamenformat wird verwendet, um eine Domäne und ein Benutzerkonto in dieser Domäne anzugeben, z. B. <i><b>DOMAIN \\ UserName</b></i>. In der folgenden Tabelle werden die Teile eines Anmeldenamens auf downer ebener Ebene zusammengefasst.



| Teil                                                           | Beispiel               |
|----------------------------------------------------------------|-----------------------|
| NetBIOS-Domänenname.<br/>                                | *DOMAIN*<br/>   |
| Trennzeichen. Ein Zeichenliteral, der schräge Schrägstrich ( \\ ).<br/> | **\\**<br/>     |
| Benutzername. Wird auch als Anmeldename bezeichnet.<br/>    | *UserName*<br/> |



 

 

 
