---
description: 'Die "rendbind"-Konstanten sind Flags, die von der itdirectory:: Bind-Methode verwendet werden, um Typen der angegebenen Authentifizierung anzugeben.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: RENDBIND_ Konstanten (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371665"
---
# <a name="rendbind_-constants"></a>Rendbind- \_ Konstanten

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die "rendbind"-Konstanten sind Flags, die von der [**itdirectory:: Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) -Methode verwendet werden, um Typen der angegebenen Authentifizierung anzugeben.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**"rendbind"- \_ Authentifizierung**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Authentifizieren Sie den Benutzer.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**rendbind \_ DefaultDomainName**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Verwenden Sie den Standard Domänen Namen.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**rendbind \_ DefaultUserName**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Standardbenutzer Namen verwenden.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**rendbind \_ DefaultPassword**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Standard Kennwort verwenden.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**rendbind \_ default-Anmelde Informationen**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Die vorherigen drei ORed sind aus Gründen der leichteren Arbeit.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Rend. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itdirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**Itdirectory:: Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




