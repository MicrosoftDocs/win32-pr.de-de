---
description: Wenn eine Anwendung die Anmelde Informations Verwaltungs-API verwendet, um Anmelde Informationen einzugeben, wird erwartet, dass der Benutzer die Informationen eingibt, die vom Betriebssystem oder von der Anwendung überprüft werden können.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Benutzernamen Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349591"
---
# <a name="user-name-formats"></a>Benutzernamen Formate

Wenn eine Anwendung die Anmelde Informations Verwaltungs-API verwendet, um Anmelde Informationen einzugeben, wird erwartet, dass der Benutzer die Informationen eingibt, die vom Betriebssystem oder von der Anwendung überprüft werden können. Der Benutzer kann Informationen zu Domänen Anmelde Informationen in einem der folgenden Formate angeben:

-   [Benutzerprinzipalname](#user-principal-name)
-   [Anmelde Name auf der gleichen Ebene](#down-level-logon-name)

## <a name="user-principal-name"></a>Benutzerprinzipalname

Das UPN-Format ( [*User Principal Name, Benutzer Prinzipal Name*](../secgloss/u-gly.md) ) wird verwendet, um einen Internet Namen anzugeben, z <b>UserName@Example.Microsoft.com</b> . b.. In der folgenden Tabelle werden die Teile eines UPN zusammengefasst.



| Teil                                                        | Beispiel                                |
|-------------------------------------------------------------|----------------------------------------|
| Der Name des Benutzerkontos. Wird auch als Anmelde Name bezeichnet.<br/> | *UserName*<br/>                  |
| Trennzeichen. Ein Zeichenliteral, das at-Zeichen (@).<br/> | @<br/>                           |
| UPN-Suffix. Wird auch als Domänen Name bezeichnet.<br/>       | *Example.Microsoft.com* <br/> |



 

Ein UPN kann implizit oder explizit definiert werden. Ein impliziter UPN hat die Form <b>UserName@DNSDomainName.com</b> . Ein impliziter UPN ist immer mit dem Benutzerkonto verknüpft, auch wenn kein expliziter UPN definiert ist. Ein expliziter UPN weist das Format auf, wobei die Namen-und suffixzeichenfolgen <i><b>Name@Suffix</b></i> explizit vom Administrator definiert werden.

## <a name="down-level-logon-name"></a>Anmelde Name Down-Level

Das Format der untergeordneten Anmelde Namen wird verwendet, um eine Domäne und ein Benutzerkonto in dieser Domäne anzugeben, z. b. <i><b>Domäne \\ Benutzername</b></i>. In der folgenden Tabelle werden die Teile eines untergeordneten Anmelde namens zusammengefasst.



| Teil                                                           | Beispiel               |
|----------------------------------------------------------------|-----------------------|
| NetBIOS-Domänen Name.<br/>                                | *DOMAIN*<br/>   |
| Trennzeichen. Ein Zeichenliterals, der umgekehrte Schrägstrich ( \\ ).<br/> | **\\**<br/>     |
| Der Name des Benutzerkontos. Wird auch als Anmelde Name bezeichnet.<br/>    | *UserName*<br/> |



 

 

 
