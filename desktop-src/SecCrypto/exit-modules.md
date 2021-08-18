---
description: Beendigungsmodule erhalten Benachrichtigungen von der Server-Engine, wenn Vorgänge wie die Ausstellung eines Zertifikats auftreten.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Beenden von Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ba8d821900ece1a4ce3eb3fcb2cc805d87274b451a3d5c8948d1e86ebf3547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140753"
---
# <a name="exit-modules"></a>Beenden von Modulen

Beendigungsmodule erhalten Benachrichtigungen von der Server-Engine, wenn Vorgänge wie die Ausstellung eines Zertifikats auftreten. Ein Exitmodul wird als [*DLL (Dynamic Link Library)*](../secgloss/d-gly.md) implementiert. Ein typischer Vorgang für ein Exitmodul ist das Veröffentlichen eines abgeschlossenen Zertifikats an einem angegebenen Speicherort (das Standardmäßige Exitmodul der Unternehmenszertifizierungsstelle veröffentlicht z. B. Benutzerzertifikate und [*Zertifikatsperrlisten*](../secgloss/c-gly.md) (Certificate Revocation Lists, CRLs) in Active Directory. Ein Exitmodul kann die [**ICertServerExit-Schnittstelle**](/windows/desktop/api/Certif/nn-certif-icertserverexit) verwenden, um mit Zertifikatdiensten zu kommunizieren. Zertifikatdienste kommunizieren mit einem Exitmodul über direkte COM-Aufrufe oder , wenn das Modul keine direkten COM-Aufrufe unterstützt, über Automation.

Ein Exitmodul kann vorhandene Zertifikateigenschaften und -erweiterungen sowie Anforderungsattribute und -eigenschaften anzeigen. Ein Exitmodul kann jedoch keine Eigenschaften ändern.

Zertifikatdienste bieten ein Standard-Exitmodul, aber Sie können auch benutzerdefinierte Exitmodule erstellen, um besondere Anforderungen zu erfüllen. Bevor Sie jedoch ein benutzerdefiniertes Exitmodul schreiben, sollten Sie das Standardmäßige Exitmodul verwenden. Darüber hinaus sollte für eine Unternehmenszertifizierungsstelle immer das Standard-Exitmodul verwendet werden, auch wenn Sie zusätzliche benutzerdefinierte Exitmodule hinzufügen können. Weitere Informationen finden Sie unter [Schreiben von benutzerdefinierten Exitmodulen.](writing-custom-exit-modules.md)

 

 
