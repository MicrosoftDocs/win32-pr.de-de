---
description: In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll exportiert wird. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Hilfsfunktionen (Zertifikatregistrierungs-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347748"
---
# <a name="helper-functions-certificate-enrollment-api"></a>Hilfsfunktionen (Zertifikatregistrierungs-API)

In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll exportiert wird. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht.

## <a name="binaryblobtostring"></a>binaryblobto String

Die [**binaryblobdestring**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) -Funktion in Xenroll.dll konvertiert ein Bytearray in eine Zeichenfolge.

Mithilfe CertEnroll.dll können Sie die [**variantbytearrayto String**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) -Methode für die [**ibinaryconverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) -Schnittstelle aufrufen.

## <a name="stringtobinaryblob"></a>stringdebinaryblob

Die [**stringdebinaryblob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) -Funktion in Xenroll.dll konvertiert eine Zeichenfolge in ein Bytearray.

Mithilfe CertEnroll.dll können Sie die [**stringdevariantbytearray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) -Methode für die [**ibinaryconverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) -Schnittstelle aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnung von Xenroll.dll zu CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**Ibinaryconverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
