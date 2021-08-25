---
title: NULL-Sitzungen
description: Manchmal kann ein Aufruf, der in der NULL-Sitzung eintreffen kann, wie ein authentifizierter Aufruf aussehen.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5476a49513019fe15afa4a30beae08104533a6621a84c4e0d1de4e9f315275ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019560"
---
# <a name="null-sessions"></a>NULL-Sitzungen

Manchmal kann ein Aufruf, der in der NULL-Sitzung eintreffen kann, wie ein authentifizierter Aufruf aussehen. Insbesondere der Aufruf der [**RpcBindingInqAuthClient-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) gibt die für den Aufruf verwendete Authentifizierungsebene und den Sicherheitsanbieter zurück. Dieser Vorgang bedeutet nicht, dass der Aufruf nicht für eine NULL-Sitzung durchgeführt wurde. Die beiden Probleme sind orthogonal. In Microsoft Windows 2000 kann ein Remoteprozeduraufruf versuchen, die Identität eines Aufrufers zu ändern und die Berechtigungen nach dem Identitätswechsel zu überprüfen. Unter Microsoft Windows XP ist es schneller, die [**RpcServerInqCallAttributes-Funktion**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) aufzugeben und nach dem **NullSession-Flag zu** überprüfen.

Ein weiterer relevanter Unterschied besteht zwischen Windows 2000 und Windows XP. Wenn nur das RPC IF ALLOW SECURE ONLY-Flag angegeben ist, werden Aufrufe für die NULL-Sitzung in Windows \_ \_ \_ \_ 2000 ausgeführt. In Windows XP werden Aufrufe für die NULL-Sitzung mit der allgemeinen Härte der Standardsicherheitseinstellungen abgelehnt, wenn dieses Flag angegeben wird. Selbst mit dem RPC IF ALLOW SECURE ONLY-Flag garantiert RPC jedoch nicht die \_ \_ \_ \_ Berechtigungsstufe des aufrufenden Benutzers. Bei allen RPC-Überprüfungen wird überprüft, ob der Benutzer über gültige Anmeldeinformationen verfügt. Es ist möglich, dass der aufrufende Benutzer das Gastkonto oder andere Konten mit geringen Berechtigungen verwendet. Stellen Sie sicher, dass der Server keine hohen Berechtigungen an sich nimmt, sobald RPC \_ IF ALLOW SECURE ONLY verwendet \_ \_ \_ wird.

 

 




