---
title: Auswählen einer Authentifizierungs Ebene
description: Wenn Sie eine Authentifizierungs Ebene auswählen, verwenden Sie die folgende Richtlinie.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471149"
---
# <a name="choosing-an-authentication-level"></a>Auswählen einer Authentifizierungs Ebene

Wenn Sie eine Authentifizierungs Ebene auswählen, verwenden Sie die folgende Richtlinie. Wenn es keine Rolle spielt, ob die gesendeten Daten abgefangen und geändert werden können und die empfangenen Daten abgefangen oder geändert werden können, verwenden Sie RPC \_ C \_ authn \_ Level None ( \_ Standardeinstellung). Wenn die Daten nicht geändert werden sollen und private Daten nicht gesendet oder empfangen werden, verwenden Sie die Pkt-Integrität der RPC- \_ C- \_ authn- \_ Ebene \_ \_ . Verwenden Sie in allen anderen Fällen die \_ Pkt-Datenschutz auf RPC-C- \_ authn- \_ Ebene \_ \_ .

Verwenden Sie nicht die Standardeinstellung RPC-c-authn- \_ \_ \_ Ebene \_ , RPC \_ c \_ authn \_ Level \_ Connect, RPC- \_ c- \_ authn- \_ Ebene \_ oder RPC- \_ c-authn-Ebene \_ \_ \_ Pkt. Ein anspruchsvoller Angreifer kann diese Authentifizierungs Ebenen unterbrechen und Sie als unwirksam erweisen. Auf jeder dieser Ebenen ist es für einen Angreifer etwas schwieriger, Daten abzufangen und zu ändern und einen Identitätswechsel vorzunehmen, aber die Sicherheit wird nicht wirklich erreicht. Da die Komplexität eines Angreifers selten bekannt ist, sind diese Optionen nicht sinnvoll.

 

 




