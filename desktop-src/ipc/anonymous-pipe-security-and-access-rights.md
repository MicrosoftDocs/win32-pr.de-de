---
description: Sie können eine Sicherheits Beschreibung für eine anonyme Pipe angeben, wenn Sie die Funktion "-Funktion" aufrufen. Die Sicherheits Beschreibung steuert den Zugriff auf die Lese-und schreibenden der Pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Sicherheit und Zugriffsrechte für anonyme Pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350119"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für anonyme Pipe

Mithilfe der Windows-Sicherheit können Sie den Zugriff auf anonyme Pipes steuern. Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).

Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für eine Pipe angeben, wenn [**Sie die Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) "-Funktion" aufrufen. Die Sicherheits Beschreibung steuert den Zugriff auf die Lese-und schreibenden der Pipe. Wenn Sie **null** angeben, erhält die Pipe eine Standard Sicherheits Beschreibung. Die ACLs in der Standard Sicherheits Beschreibung für eine Pipe stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.

Um die Sicherheits Beschreibung eines Pipe abzurufen, rufen Sie die [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion auf. Um die Sicherheits Beschreibung einer Pipe zu ändern, müssen Sie die Funktion [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) aufrufen.

Die Funktion " [**kreatepipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) " gibt zwei Handles an die anonyme Pipe zurück: ein Lese Handle mit generischem \_ Lese-und Synchronisierungs Zugriff und ein Schreib Handle mit generischem \_ Schreib-und Synchronisierungs Zugriff. \_Für den generischen Lesezugriff und den generischen \_ Schreibzugriff wird dieselbe Zugriffsrechte Zuordnung wie für Named Pipes verwendet.

Der generische \_ Lesezugriff für eine anonyme Pipe kombiniert die Rechte zum Lesen von Daten aus der Pipe, zum Lesen von Pipe-Attributen, zum Lesen erweiterter Attribute und zum Lesen der DACL der Pipe.

\_Der generische Schreibzugriff für eine anonyme Pipe kombiniert die Rechte zum Schreiben von Daten in die Pipe, zum Anfügen von Daten an die Pipe, zum Schreiben von Pipe-Attributen, zum Schreiben erweiterter Attribute und zum Lesen der DACL der Pipe.

 

 
