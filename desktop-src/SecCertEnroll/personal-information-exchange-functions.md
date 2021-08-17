---
description: In jedem der folgenden Abschnitte wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von PFX-Nachrichten (Personal Information Exchange) exportiert wird.
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funktionen für personenbezogene Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e7cddcda00131b64c5fe6122d777695bbab4f80cbac8e71648a2197fed036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774683"
---
# <a name="personal-information-exchange-functions"></a>Funktionen für personenbezogene Exchange

In jedem der folgenden Abschnitte wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von PFX-Nachrichten (Personal Information Exchange) exportiert wird. In jedem Abschnitt wird auch erläutert, wie sie CertEnroll.dll, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

Die [**createFilePFXWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) in Xenroll.dll eine Zertifikatkette und einen [*privaten*](/windows/desktop/SecGloss/p-gly) Schlüssel im PFX-Format in einer Datei speichert.

Die CertEnroll.dll-Bibliothek implementiert nicht direkt Funktionen zum Kopieren der PFX-Nachricht in eine Datei. Sie können jedoch die [**CreatePFX-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) auf der [**IX509Enrollment-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) verwenden, um eine codierte PFX-Nachricht zu erstellen und eine benutzerdefinierte Funktion zu schreiben, um die Nachricht in einer Datei zu speichern.

## <a name="createpfxwstr"></a>createPFXWStr

Die [**createPFXWStr-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) in Xenroll.dll eine Zertifikatkette und einen privaten Schlüssel in einer PFX-Formatzeichenfolge speichert.

Sie können die [**CreatePFX-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) auf der [**IX509Enrollment-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) verwenden, um eine codierte PFX-Nachricht zu erstellen, die die Zertifikatkette und den Schlüssel enthält. Sie können ein Kennwort, Exportoptionen und einen Codierungstyp angeben. Um eine Zeichenfolge abzurufen, die der von [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr)zurückgegebenen entspricht, übergeben Sie das XCN CRYPT STRING BINARY-Flag in im Encoding-Parameter der \_ \_ \_  [**CreatePFX-Methode.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
