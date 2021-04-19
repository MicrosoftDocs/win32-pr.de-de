---
description: Ein Dienst sollte nicht auf den Stamm des aktuellen HKEY- \_ \_ Benutzers oder der HKEY- \_ Klasse zugreifen \_ , insbesondere bei der Identität eines Benutzers. Verwenden Sie stattdessen die Funktion "regopencurrentuser" oder "regopenuserclassesroot".
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Dienste und die Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363714"
---
# <a name="services-and-the-registry"></a>Dienste und die Registrierung

Ein Dienst sollte nicht auf den Stamm des **aktuellen HKEY- \_ \_ Benutzers** oder der **HKEY- \_ Klasse \_** zugreifen, insbesondere bei der Identität eines Benutzers. Verwenden Sie stattdessen die Funktion " [**regopencurrentuser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) " oder " [**regopenuserclassesroot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) ".

Wenn Sie versuchen, auf **HKEY \_ Current \_ User** -oder **HKEY- \_ Klassen \_** Stamm von einem Dienst zuzugreifen, tritt möglicherweise ein Fehler auf, oder es scheint zu funktionieren, aber es ist ein zugrunde liegender Fehler aufgetreten, der zu Problemen beim Laden oder Entladen des Benutzerprofils führen kann.

 

 
