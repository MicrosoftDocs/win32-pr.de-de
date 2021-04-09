---
description: Die duplikatandle-Funktion erstellt ein doppeltes handle, das von einem anderen angegebenen Prozess verwendet werden kann.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Objekt Duplizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042594"
---
# <a name="object-duplication"></a>Objekt Duplizierung

Die [**duplikatandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion erstellt ein doppeltes handle, das von einem anderen angegebenen Prozess verwendet werden kann. Diese Methode der Freigabe von Objekt Handles ist komplexer als die Verwendung benannter Objekte oder Vererbung. Hierfür ist eine Kommunikation zwischen dem Erstellungsprozess und dem Prozess erforderlich, in den das Handle dupliziert wird. Die erforderlichen Informationen (der Handle-Wert und die Prozess-ID) können von jeder prozessübergreifenden Kommunikationsmethode (z. b. Named Pipes oder benannte Shared Memory) kommuniziert werden.

 

 
