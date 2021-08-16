---
description: Sie können eine Sicherheitsbeschreibung für eine anonyme Pipe angeben, wenn Sie die CreatePipe-Funktion aufrufen. Der Sicherheitsdeskriptor steuert den Zugriff auf die Lese- und Schreibenden der Pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Sicherheit und Zugriffsrechte für anonyme Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b54869584a70bfbe886740e979c44864d852de0df23e311eb4aad89c321662c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756357"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für anonyme Pipes

mit Windows Sicherheit können Sie den Zugriff auf anonyme Pipes steuern. Weitere Informationen zur Sicherheit finden Sie unter [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).

Sie können eine [Sicherheitsbeschreibung](/windows/desktop/SecAuthZ/security-descriptors) für eine Pipe angeben, wenn Sie die [**CreatePipe-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) aufrufen. Der Sicherheitsdeskriptor steuert den Zugriff auf die Lese- und Schreibenden der Pipe. Wenn Sie **NULL** angeben, ruft die Pipe einen Standardsicherheitsdeskriptor ab. Die ACLs im Standardsicherheitsdeskriptor für eine Pipe stammen aus dem primären Token oder Identitätswechseltoken des Erstellers.

Rufen Sie die [**GetSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) auf, um die Sicherheitsbeschreibung einer Pipe abzurufen. Um die Sicherheitsbeschreibung einer Pipe zu ändern, rufen Sie die [**SetSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) auf.

Die [**CreatePipe-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) gibt zwei Handles an die anonyme Pipe zurück: ein Lesehandle mit GENERIC \_ READ- und SYNCHRONIZE-Zugriff und ein Schreibhandle mit GENERIC \_ WRITE- und SYNCHRONIZE-Zugriff. GENERIC \_ READ- und GENERIC \_ WRITE-Zugriff verwenden die gleiche Zugriffsberechtigungszuordnung wie für Named Pipes.

Generischer \_ LESEzugriff für eine anonyme Pipe kombiniert die Rechte zum Lesen von Daten aus der Pipe, Lesen von Pipeattributen, Lesen erweiterter Attribute und Lesen der DACL der Pipe.

Der GENERISCHE \_ WRITE-Zugriff für eine anonyme Pipe kombiniert die Rechte zum Schreiben von Daten in die Pipe, zum Anfügen von Daten, zum Schreiben von Pipeattributen, zum Schreiben erweiterter Attribute und zum Lesen der DACL der Pipe.

 

 
