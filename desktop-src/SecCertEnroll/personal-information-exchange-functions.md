---
description: In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von PFX-Nachrichten (Personal Information Exchange) exportiert wird.
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funktionen für den persönlichen Informationsaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352210"
---
# <a name="personal-information-exchange-functions"></a>Funktionen für den persönlichen Informationsaustausch

In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll zum Verwalten von PFX-Nachrichten (Personal Information Exchange) exportiert wird. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht.

## <a name="createfilepfxwstr"></a>"kreatefilepfxwstr"

Die [**Funktion "**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) Funktion in Xenroll.dll" speichert eine Zertifikat Kette und einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) in einer Datei im PFX-Format.

Die CertEnroll.dll Bibliothek implementiert nicht direkt Funktionen zum Kopieren der PFX-Nachricht in eine Datei. Sie können jedoch [**die Methode "**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) Methode" in der [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle verwenden, um eine codierte PFX-Nachricht zu erstellen und eine benutzerdefinierte Funktion zum Speichern der Nachricht in einer Datei zu schreiben.

## <a name="createpfxwstr"></a>"kreatepfxwstr"

Die Funktion " [**epatepfxwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) " in Xenroll.dll speichert eine Zertifikat Kette und einen privaten Schlüssel in einer PFX-Format Zeichenfolge.

Sie können [**die Methode "**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) Methode" in der [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle verwenden, um eine codierte PFX-Nachricht zu erstellen, die die Zertifikatskette und den Schlüssel enthält. Sie können ein Kennwort, Exportoptionen und den Codierungstyp angeben. Um eine Zeichenfolge abzurufen, die der von " [**kreatepfxwstr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr)" zurückgegebenen entspricht, übergeben Sie das XCN \_ crypt-Zeichen folgen \_ \_ Binär Flag im- [](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) *Codierungs* Parameter der Methode "Methode".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
