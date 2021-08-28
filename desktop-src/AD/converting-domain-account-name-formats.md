---
title: Konvertieren von Formaten für Domänenkontonamen
description: Die Microsoft Win32-Funktionen für die Arbeit mit dem Dienststeuerungs-Manager (Service Control Manager, SCM) auf einem Hostserver verwenden \ 0034; \\ Domänenbenutzername \ 0034; Format für Dienstkonten.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa1b3664cc0ad372f82b498153862e69013fb1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881594"
---
# <a name="converting-domain-account-name-formats"></a>Konvertieren von Formaten für Domänenkontonamen

Die Microsoft Win32-Funktionen für die Arbeit mit dem Dienststeuerungs-Manager (Service Control Manager, SCM) auf einem Hostserver verwenden das Format &lt; "Domänenbenutzername" &gt; \\ &lt; &gt; für Dienstkonten. Wenn Sie z. B. die [**QueryServiceConfig-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) aufrufen, um das Benutzerkonto abzurufen, unter dem Ihr Dienst ausgeführt wird, gibt die Funktion den Namen im Format "Fabrikam \\ jeffsmith" zurück. Zum Binden an das Benutzerkonto im Verzeichnis, z. B. zum Ändern des Kontokennworts, ist der Distinguished Name des Kontos erforderlich, der das Format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM" auf hat.

Um zwischen den verschiedenen Namensformaten zu konvertieren, verwenden Sie die [**TranslateName-Funktion,**](/windows/desktop/api/secext/nf-secext-translatenamea) die einen Namen in andere Formate konvertieren kann, z. B. einen Benutzerprinzipalnamen (UPN).

 

 
