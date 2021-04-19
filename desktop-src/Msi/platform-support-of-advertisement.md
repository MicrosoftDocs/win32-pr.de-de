---
description: Der Windows Installer unterstützt Ankündigungen von Anwendungen und Features.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Platt Form Unterstützung für Ankündigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355729"
---
# <a name="platform-support-of-advertisement"></a>Platt Form Unterstützung für Ankündigungen

Der Windows Installer unterstützt Ankündigungen von Anwendungen und Features.

Die folgenden Ankündigungs Funktionen sind unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP und Windows 2000 verfügbar.

-   Tastenkombinationen und deren Symbole.

-   Erweiterungen und ihre Symbole, die in der [ProgID-Tabelle](progid-table.md)angegeben sind.

-   Shell-und Befehls Verben, die unterhalb des ProgID-Schlüssels registriert sind

-   CLSID-Kontexte und InprocHandler.

-   Die Installation von on-Demand über OLE ist nur Programm gesteuert über [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) und **CreateObject-Funktion (Visual Basic)** oder **GetObject-Funktion (Visual Basic)** verfügbar.

> [!Note]
> Die AppID-und TypeLib-Informationen werden nur geschrieben, wenn eine angekündigte Komponente installiert ist.
> 
> Zur Unterstützung von Dateinamen Erweiterungen muss die Anwendung von einem Administrator mit Gruppenrichtlinie Active Directory veröffentlicht werden.

## <a name="remarks"></a>Bemerkungen

Die Installation des Produkts erfordert möglicherweise keinen Neustart, aber alle angekündigten Verknüpfungen funktionieren erst, wenn der Computer neu gestartet wird. Die angekündigten Verknüpfungen für nachfolgende Installationen funktionieren ohne Neustart.

Um sicherzustellen, dass angekündigte Verknüpfungen ordnungsgemäß funktionieren, sollte der Paket Ersteller am Ende der Installation einen erzwungenen Neustart planen.

Um unnötige Neustarts des Systems zu vermeiden, planen Sie einen Neustart so, dass er nur ausgeführt wird, wenn keine Version des Windows Installer installiert ist.

Bedingte Anweisungen können die [**shelladvtsupport**](shelladvtsupport.md) -Eigenschaft und die [**Version9X**](version9x.md) -Eigenschaft überprüfen. Weitere Informationen zum Planen eines bedingten erzwungenen Neustarts finden Sie unter [System Neustarts](system-reboots.md) und [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md).

 

 
