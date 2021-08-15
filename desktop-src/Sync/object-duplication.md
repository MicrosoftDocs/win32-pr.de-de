---
description: Die DuplicateHandle-Funktion erstellt ein doppeltes Handle, das von einem anderen angegebenen Prozess verwendet werden kann.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Objektduplizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927f9d3b60f358623e66a067e75992e71c76ca5fe072a9749c9bbc217bfa2ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886340"
---
# <a name="object-duplication"></a>Objektduplizierung

Die [**DuplicateHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) erstellt ein doppeltes Handle, das von einem anderen angegebenen Prozess verwendet werden kann. Diese Methode der Freigabe von Objekthandles ist komplexer als die Verwendung benannter Objekte oder vererbung. Sie erfordert die Kommunikation zwischen dem Erstellungsprozess und dem Prozess, in den das Handle dupliziert wird. Die erforderlichen Informationen (der Handlewert und der Prozessbezeichner) können von jeder der prozessübergreifenden Kommunikationsmethoden wie Named Pipes oder benanntem freigegebenem Speicher übermittelt werden.

 

 
