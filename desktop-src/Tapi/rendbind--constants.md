---
description: Die RENDBIND-Konstanten sind Flags, die von der ITDirectory::Bind-Methode verwendet werden, um die angegebenen Authentifizierungstypen anzugeben.
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: RENDBIND_ Konstanten (Rend.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c618ed2cf5d9dda4c2ee14b331e3603f8021e9c5f4755e38ecfb5929b5f45c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760863"
---
# <a name="rendbind_-constants"></a>\_RENDBIND-Konstanten

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die RENDBIND-Konstanten sind Flags, die von der [**ITDirectory::Bind-Methode**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) verwendet werden, um die angegebenen Authentifizierungstypen anzugeben.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND \_ AUTHENTICATE**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Authentifizieren des Benutzers.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Verwenden Sie den Standarddomänennamen.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Verwenden Sie den Standardbenutzernamen.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Verwenden Sie das Standardkennwort.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Die vorherigen drei OR wurden aus Gründen der Einfachheit zusammengehörig.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Rend.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




