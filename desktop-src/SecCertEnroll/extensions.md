---
description: Das X.509 Version 3-Zertifikatformat identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Erweiterungen (Zertifikatregistrierungs-API)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 534c3cf9268f21c36d982a627de2e1b293ffdca1e1fd4ffc2acd0db9f7d6059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867940"
---
# <a name="extensions-certificate-enrollment-api"></a>Erweiterungen (Zertifikatregistrierungs-API)

Das X.509 Version 3-Zertifikatformat identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können. Die Erweiterungen bieten erweiterte Informationen zur Schlüsselverwendung, Zertifikatrichtlinien und Einschränkungen, alternative Namensformulare und vieles mehr. Sie können die [**IX509Extension-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) verwenden, um einen Erweiterungswert zu definieren. Viele der allgemeinen Erweiterungen können mithilfe vordefinierter Schnittstellen erstellt werden, die von **IX509Extension** abgeleitet werden. Eine Auflistung von Erweiterungen wird einer Zertifikatanforderung hinzugefügt, indem die Auflistung in die Anforderungsattribute eingeschlossen wird. Weitere Informationen finden Sie in den folgenden Themen:

-   [Unterstützte Erweiterungen](supported-extensions.md)
-   [PKCS \# 10-Erweiterungen](pkcs--10-extensions.md)
-   [CMC-Erweiterungen](cmc-extensions.md)

 

 



