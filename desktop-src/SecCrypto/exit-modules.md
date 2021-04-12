---
description: Exit-Module empfangen Benachrichtigungen von der Server-Engine, wenn Vorgänge wie das Ausstellen eines Zertifikats stattfinden.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Beenden von Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217151"
---
# <a name="exit-modules"></a>Beenden von Modulen

Exit-Module empfangen Benachrichtigungen von der Server-Engine, wenn Vorgänge wie das Ausstellen eines Zertifikats stattfinden. Ein Beendigungs Modul wird als [*Dynamic Link Library*](../secgloss/d-gly.md) (dll) implementiert. Eine typische Operation für ein Beendigungs Modul besteht darin, ein vollständiges Zertifikat an einem angegebenen Speicherort zu veröffentlichen (das standardmäßige Beendigungs Modul der Unternehmens Zertifizierungsstelle, beispielsweise, veröffentlicht Benutzerzertifikate und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs) für die Active Directory). Ein Beendigungs Modul kann die [**icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) -Schnittstelle für die Kommunikation mit Zertifikat Diensten verwenden. Die Zertifikat Dienste kommunizieren mit einem Beendigungs Modul mithilfe von direkten com-aufrufen oder, wenn das Modul direkte com-Aufrufe nicht unterstützt, mithilfe von Automation.

Ein Beendigungs Modul zeigt möglicherweise vorhandene Zertifikat Eigenschaften und-Erweiterungen an und kann auch Anforderungs Attribute und-Eigenschaften anzeigen. Ein Beendigungs Modul kann jedoch keine Eigenschaften ändern.

Die Zertifikat Dienste stellen ein Standard Beendigungs Modul bereit. Sie können jedoch auch benutzerdefinierte Beendigungs Module erstellen, um besondere Anforderungen zu erfüllen. Bevor Sie jedoch ein benutzerdefiniertes Beendigungs Modul schreiben, sollten Sie das standardmäßige Beendigungs Modul verwenden. Außerdem sollte für eine Unternehmens Zertifizierungsstelle das standardmäßige Beendigungs Modul immer verwendet werden, auch wenn Sie zusätzliche, benutzerdefinierte Beendigungs Module hinzufügen können. Weitere Informationen finden Sie unter [Schreiben von benutzerdefinierten Exit-Modulen](writing-custom-exit-modules.md).

 

 
