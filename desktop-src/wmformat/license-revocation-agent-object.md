---
title: Lizenz Sperr-Agent-Objekt
description: Lizenz Sperr-Agent-Objekt
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media-Format-SDK, Lizenz Sperr-agentobjekte
- Advanced Systems Format (ASF), Lizenz Sperr-agentobjekte
- ASF (Advanced Systems Format), Lizenz Sperr-agentobjekte
- Objekte, Lizenz Sperr-agentobjekte
- Lizenz Sperrung, Lizenz Sperr-agentobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389844"
---
# <a name="license-revocation-agent-object"></a>Lizenz Sperr-Agent-Objekt

Das Lizenz Sperr-Agent-Objekt verwaltet die Clientseite der Lizenz Sperrung. Der Lizenz Widerruf ist der Prozess, mit dem ein Lizenzserver Lizenzen aus dem Lizenz Speicher auf dem Client Computer entfernen kann. Der Prozess umfasst das übergeben mehrerer Nachrichten zwischen der Client Anwendung und dem Lizenzserver. Die Methoden, die für dieses Objekt verfügbar gemacht werden, verarbeiten und generieren diese Nachrichten.

Das Lizenz Sperr-Agent-Objekt wird von der [**wmkreatelicenserevocationagent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) -Funktion erstellt, mit der ein Zeiger auf eine [**iwmlicenserevocationagent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) -Schnittstelle festgelegt wird. **IUnknown** und **iwmlicenserevocationagent** sind die einzigen Schnittstellen, die von diesem Objekt unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> </dl>

 

 




