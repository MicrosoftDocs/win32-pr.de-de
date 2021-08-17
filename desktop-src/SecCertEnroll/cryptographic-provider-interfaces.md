---
description: Die folgenden Schnittstellen können verwendet werden, um Informationen zu Kryptografieanbietern abzurufen.
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: Kryptografieanbieterschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e39e42f17efdeae353b02723522e744031a394e8faa8a4be986831087561e4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976910"
---
# <a name="cryptographic-provider-interfaces"></a>Kryptografieanbieterschnittstellen

Die folgenden Schnittstellen können verwendet werden, um Informationen zu Kryptografieanbietern abzurufen.



| Schnittstelle                                    | BESCHREIBUNG                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | Stellt einen von einem Kryptografieanbieter implementierten Algorithmus dar.             |
| [**ICspAlgorithms**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | Verwaltet eine Auflistung von [**ICspAlgorithm-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) |
| [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | Bietet Zugriff auf allgemeine Informationen zu einem Kryptografieanbieter.       |
| [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | Verwaltet eine Auflistung von [**ICspInformation-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)  |
| [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | Enthält Informationen zu einem Kryptografieanbieter/Algorithmuspaar.          |
| [**ICspStatuses**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | Verwaltet eine Auflistung von [**ICspStatus-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



