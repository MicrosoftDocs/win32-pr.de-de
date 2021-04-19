---
description: Das X. 509 Version 3-Zertifikat Format identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können.
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
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362832"
---
# <a name="extensions-certificate-enrollment-api"></a>Erweiterungen (Zertifikatregistrierungs-API)

Das X. 509 Version 3-Zertifikat Format identifiziert mehrere Erweiterungen, die einem Zertifikat hinzugefügt werden können. Die Erweiterungen bieten erweiterte Informationen zu Schlüssel Verwendung, Zertifikat Richtlinien und-Einschränkungen, Alternativen namens Formularen und mehr. Mit der [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle können Sie einen Erweiterungs Wert definieren. Viele der allgemeinen Erweiterungen können mithilfe von vordefinierten Schnittstellen erstellt werden, die von **IX509Extension** abgeleitet werden. Eine Auflistung von Erweiterungen wird einer Zertifikat Anforderung hinzugefügt, indem die Auflistung in die Anforderungs Attribute eingeschlossen wird. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Unterstützte Erweiterungen](supported-extensions.md)
-   [PKCS \# 10-Erweiterungen](pkcs--10-extensions.md)
-   [CMC-Erweiterungen](cmc-extensions.md)

 

 



