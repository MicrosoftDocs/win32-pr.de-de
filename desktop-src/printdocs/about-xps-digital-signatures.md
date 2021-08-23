---
description: Dieser Abschnitt bietet eine Übersicht über die XPS Digital Signature-API.
ms.assetid: 895974df-d5e8-4974-b057-ec7e5e59d805
title: Informationen zur XPS Digital Signature-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcfbd6000df56d96afbc86a3cd0111c02a128c3c23c0d0de59717da5f4e9ac6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950940"
---
# <a name="about-xps-digital-signature-api"></a>Informationen zur XPS Digital Signature-API

XPS-Dokumente können digitale Signaturen enthalten, damit Benutzer ein Dokument signieren, die Identität des Signaturers überprüfen und angeben können, ob sich ein XPS-Dokument seit der Signatur geändert hat. Eine native Windows-Anwendung kann die Schnittstellen der XPS Digital Signature-API verwenden, um Digitale Signaturvorgänge für ein XPS-Dokument durchzuführen. Dieser Abschnitt bietet eine Übersicht über die XPS Digital Signature-API.

Die [**IXpsSignatureManager-Schnittstelle**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) verwaltet die Vorgänge für digitale Signaturen in einem XPS-Dokument. Bevor eine Anwendung auf die digitalen Signaturen eines XPS-Dokuments zugreifen kann, muss die Anwendung [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um einen **IXpsSignatureManager** zu erstellen, und dann [**IXpsSignatureManager::LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) oder [**IXpsSignatureManager::LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) aufrufen, um das XPS-Dokument zu laden. Weitere Informationen zu diesem Initialisierungsprozess finden Sie unter [Initialisieren des Signatur-Managers.](initialize-the-signature-manager.md)

Nachdem ein XPS-Dokument in eine [**IXpsSignatureManager-Schnittstelle**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) geladen wurde, kann eine Anwendung dann auf die digitalen Signaturen und Digitalen Signaturanforderungen des Dokuments zugreifen. Sie können über eine [**IXpsSignature-Schnittstelle über die IXpsSignatureCollection-Schnittstelle**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) des Signatur-Managers auf die digitalen [**Signaturen**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection) zugreifen. Eine Anwendung kann der Sammlung auch **IXpsSignature-Schnittstellen** hinzufügen und daraus entfernen. Auf Signaturanforderungen wird [**mithilfe von IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) zugegriffen, die in einer [**IXpsSignatureRequestCollection-Schnittstelle gesammelt**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection) werden. Die **IXpsSignatureRequestCollection** ist Teil einer [**IXpsSignatureBlock-Schnittstelle,**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) die in der [**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection) des Signatur-Managers gesammelt werden.

Anwendungen können die [**IXpsSigningOptions des**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) Signatur-Managers verwenden, um auf optionen für digitale Signaturen zu zugreifen und diese zu festlegen.

Beispiele für den Zugriff auf die digitalen Signaturen eines XPS-Dokuments finden Sie unter [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der XPS Digital-Signatur-API](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[REFERENZ ZUR XPS Digital Signature-API](xps-digital-signatures-programming-reference.md)
</dt> <dt>

[Verpackung](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Standard-ECMA-376, Office Open XML-Dateiformate](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
