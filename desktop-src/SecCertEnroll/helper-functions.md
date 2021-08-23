---
description: In jedem der folgenden Abschnitte wird eine Funktion erläutert, die von Xenroll.dll. In jedem Abschnitt wird auch erläutert, wie sie CertEnroll.dll, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Hilfsfunktionen (Zertifikatregistrierungs-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99282099f93482e3064a00eed146464a8d537e70d803b3b51389f92d9f93912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669830"
---
# <a name="helper-functions-certificate-enrollment-api"></a>Hilfsfunktionen (Zertifikatregistrierungs-API)

In jedem der folgenden Abschnitte wird eine Funktion erläutert, die von Xenroll.dll. In jedem Abschnitt wird auch erläutert, wie sie CertEnroll.dll, um die Funktion zu ersetzen, oder gibt an, dass keine Zuordnung zwischen den beiden Bibliotheken vorhanden ist.

## <a name="binaryblobtostring"></a>binaryBlobToString

Die [**binaryBlobToString-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) in Xenroll.dll ein Bytearray in eine Zeichenfolge konvertiert.

Mit CertEnroll.dll können Sie die [**VariantByteArrayToString-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) für die [**IBinaryConverter-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) aufrufen.

## <a name="stringtobinaryblob"></a>stringToBinaryBlob

Die [**stringToBinaryBlob-Funktion**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) in Xenroll.dll konvertiert eine Zeichenfolge in ein Bytearray.

Mit CertEnroll.dll können Sie die [**StringToVariantByteArray-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) für die [**IBinaryConverter-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
