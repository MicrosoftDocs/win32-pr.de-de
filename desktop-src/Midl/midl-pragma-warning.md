---
title: midl_pragma Warnungsattribut
description: Verwenden Sie die \_ Midl-Pragmawarnungsoption, um das Verhalten von MIDL-Warnmeldungen zur Kompilierzeit vorübergehend zu überschreiben.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma Warnungsattribut MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae8e902d1e58ff216f36ae8003dc8f3f553a32005136ef2a86201bd17279107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067090"
---
# <a name="midl_pragma-warning-attribute"></a>\_midl-Pragmawarnungsattribut

Verwenden Sie die **\_ Midl-Pragmawarnungsoption,** um das Verhalten von MIDL-Warnmeldungen zur Kompilierzeit vorübergehend zu überschreiben.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*\_Warnungsoption* 
</dt> <dd>

Die Warnungsoption kann eine der folgenden Optionen sein: disable, enable, default.

</dd> <dt>

*\_Meldungsliste* 
</dt> <dd>

Eine Durch Leerzeichen getrennte Liste von Nachrichtennummern.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Pragma kann wie ein C-Compiler-Pragma verwendet werden. Das heißt, es deaktiviert, aktiviert oder kehrt zum Standardverhalten für eine bestimmte MIDL-Warnung zurück.

## <a name="examples"></a>Beispiele

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




