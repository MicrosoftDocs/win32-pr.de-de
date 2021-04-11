---
description: Dieser Abschnitt enthält eine Übersicht über die XPS-API für digitale Signaturen.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Informationen über die XPS Digital Signature-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba2bad4ef10d8800e9a4cb59289fccb75cc2d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131601"
---
# <a name="about-xps-digital-signature-api"></a>Informationen über die XPS Digital Signature-API

XPS-Dokumente können digitale Signaturen aufweisen, damit Benutzer ein Dokument signieren, die Identität des Signatur Gebers überprüfen und angeben können, ob ein XPS-Dokument seit der Signierung geändert wurde. Eine systemeigene Windows-Anwendung kann die Schnittstellen der XPS Digital Signature-API verwenden, um digitale Signatur Vorgänge in einem XPS-Dokument auszuführen. Dieser Abschnitt enthält eine Übersicht über die XPS-API für digitale Signaturen.

Die [**ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) -Schnittstelle verwaltet die digitalen Signatur Vorgänge in einem XPS-Dokument. Bevor eine Anwendung auf die digitalen Signaturen eines XPS-Dokuments zugreifen kann, muss die Anwendung [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um einen **ixpssignaturemanager** zu erstellen, und dann [**ixpssignaturemanager:: loadpackagefile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) oder [**ixpssignaturemanager:: loadpackagestream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) aufrufen, um das XPS-Dokument zu laden. Weitere Informationen zu diesem Initialisierungs Prozess finden Sie unter [Initialisieren des Signatur-Managers](initialize-the-signature-manager.md).

Nachdem ein XPS-Dokument in eine [**ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) -Schnittstelle geladen wurde, kann eine Anwendung auf die digitalen Signaturen und digitale Signatur Anforderungen des Dokuments zugreifen. Sie können auf die digitalen Signaturen zugreifen, indem Sie eine [**ixpssignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) -Schnittstelle von der [**ixpssignatuerinnerungs**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) -Schnittstelle des Signatur-Managers verwenden. Eine Anwendung kann auch **ixpssignature** -Schnittstellen aus der Auflistung hinzufügen und entfernen. Auf Signatur Anforderungen wird mithilfe von [**ixpssignaturerequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) zugegriffen, die in einer [**ixpssignaturerequestcollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) -Schnittstelle gesammelt werden. Die **ixpssignaturerequestcollection** ist Teil einer [**ixpssignatureblock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) -Schnittstelle, die in der [**ixpssignatureblockcollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) des Signatur-Managers erfasst wird.

Anwendungen können die [**ixpssigningoptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) des Signatur-Managers verwenden, um auf digitale Signatur Optionen zuzugreifen und diese festzulegen.

Beispiele für den Zugriff auf die digitalen Signaturen eines XPS-Dokuments finden Sie unter [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der XPS Digital-Signatur-API](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[XPS-API-Referenz für digitale Signaturen](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Verpackung](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Standard-ECMA-376, Office Open XML-Dateiformate](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
